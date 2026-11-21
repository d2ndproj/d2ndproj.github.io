---
layout: post
title: "How to Create Related Posts"
date: 2026-11-22
categories: [tutorial]
---

You have probably seen it on other blogs: at the bottom of a post, a small list that says "Related Posts" with links to similar articles. It keeps readers on your site longer, and it helps Google understand what your posts are about.

Here is how to add it to a Jekyll blog. There are two steps.

## Step 1: Give your posts a category

A category is just a label. Open a post file and add one line to the top part (the front matter):

```yaml
---
layout: post
title: "My Post Title"
date: 2026-11-22
categories: [tutorial]
---
```

Posts with the same category will link to each other. For example, all my tutorial posts have `categories: [tutorial]`, and all my personal writing posts have `categories: [writing]`. You can use any words you like as categories.

## Step 2: Add a related posts section to your post layout

Your theme decides what a post page looks like. To add something new, you make your own copy of the post layout. Create a file called `_layouts/post.html` in your repository and paste in your theme's post layout, plus this block after the article text:

{% raw %}
```liquid
{%- if page.categories -%}
  {%- assign cat = page.categories[0] -%}
  {%- assign related = site.posts | where_exp: "post", "post.categories contains cat" | where_exp: "post", "post.url != page.url" -%}
  {%- if related.size > 0 -%}
  <div class="related-posts">
    <h2>Related Posts</h2>
    <ul>
      {%- for post in related limit:3 -%}
      <li><a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></li>
      {%- endfor -%}
    </ul>
  </div>
  {%- endif -%}
{%- endif -%}
```
{% endraw %}

Here is what that code does, line by line:

- It takes the current post's first category.
- It looks through all your posts and keeps the ones with the same category.
- It skips the post you are already reading.
- It shows up to 3 of them as a list of links under a "Related Posts" heading.
- If a post has no related posts, it shows nothing at all.

## Step 3: Save and wait

Commit the files. GitHub rebuilds your site in about a minute, and every post will now show its related posts at the bottom.

That is all. From now on, every new post you write just needs a category line, and it will automatically join the related posts of the older ones. No extra work per post.
