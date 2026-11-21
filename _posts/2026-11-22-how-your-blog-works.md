---
layout: post
title: "How Your Blog Works"
date: 2026-11-22
---

Your blog has three parts working together. Once you see how they fit, everything else makes sense.

**Jekyll** is the tool that builds your blog. You write posts in simple text files, and Jekyll turns them into web pages.

**GitHub Pages** is the free hosting. It takes your files, runs Jekyll, and puts the finished site on the internet at `d2ndproj.github.io`.

**Your repository** is where the files live. It is called `d2ndproj.github.io`, on the `main` branch.

Here are the files inside it:

- `_config.yml` — the settings file. It holds your blog title, description, theme, and link style.
- `index.md` — your home page. It lists all your posts.
- `about.md` — your About page.
- `_posts/` — a folder with one file per post.
- `README.md` — an empty file GitHub created. You can ignore it.

The theme is called **Minima**. It decides how your blog looks: the layout, the fonts, the colours. You do not need to touch it.

The flow is always the same: write a file, save it to the repository, and GitHub builds the site. About a minute later, your change is live.
