---
layout: post
title: "How Publishing Works"
date: 2026-11-22
---

When you save a file to your repository, your blog does not update instantly. It goes through a small process first. Here is what happens.

## Step 1: You save a file

You create, edit, or delete a file and click **Commit changes**. That save is called a commit, and it goes to the `main` branch of your repository.

## Step 2: GitHub builds your site

GitHub notices the change and starts a build. You can watch it on the **Actions** tab of your repository. The workflow is called **pages build and deployment** and it takes about 40 seconds.

- Green tick: the build worked. Your site is updating.
- Red cross: the build failed. This usually means a small mistake in a file, like a missing quote in the settings. Check the file you just changed.

## Step 3: Your site is live

A minute or so after the build finishes, your change is live at `d2ndproj.github.io`.

## How your links are built

Your links come from one setting in `_config.yml`:

```yaml
permalink: /:title/
```

This means a post's link is just its title: `/starting-a-blog/`. Short and clean, with no date and no `.html`.

There is one more setting worth knowing:

```yaml
future: true
```

GitHub builds your site using UTC time. You are in Jakarta, which is 7 hours ahead. Without this setting, a post dated "today" in Jakarta could look like "tomorrow" to the server, and Jekyll would hide it. This setting stops that from happening.

## If your change does not show up

Wait two minutes, then do a hard refresh in your browser: **Ctrl + Shift + R** on Windows, or **Cmd + Shift + R** on Mac. The site is sometimes cached, and a hard refresh loads the newest version.
