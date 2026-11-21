---
layout: post
title: "How to Write a New Post"
date: 2026-11-22
categories: [tutorial]
---

Writing a new post is easy. You have two ways to do it.

## Way 1: Ask me

Just tell me the title and what you want to say, and I will write the post, add it to your blog, and publish it for you. This is the easiest way.

## Way 2: Do it yourself on GitHub

1. Go to your repository at `github.com/d2ndproj/d2ndproj.github.io`.
2. Open the `_posts` folder.
3. Click **Add file**, then **Create new file**.
4. Name the file like this: `2026-11-22-my-post-title.md` — the date first, then a short title with dashes instead of spaces, ending in `.md`.
5. At the top of the file, write this:

```yaml
---
layout: post
title: "My Post Title"
date: 2026-11-22
---
```

6. Write your post below that, in Markdown.
7. Click **Commit changes**. GitHub will build your site, and in about a minute your post is live.

## Writing in Markdown

Markdown is just plain text with a few simple marks:

- `# Heading` makes a big heading. `##` makes a smaller one.
- `**bold**` makes text **bold**. `*italic*` makes text *italic*.
- `[link text](https://example.com)` makes a link.
- Leave a blank line between paragraphs.

That is all you need. Write like you normally would, and use the marks when you want a heading or bold text.
