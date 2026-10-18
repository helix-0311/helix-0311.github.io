# How to post

This file is in the repo but not on the site (`_config.yml` excludes it).

## Publish a post

1. Make a file in `_posts/`. The name is the date plus a short slug:
   `_posts/2026-10-25-why-d100.md`
2. Start it with this header:

   ```
   ---
   layout: post
   title: "Why d100"
   date: 2026-10-25
   ---
   ```

3. Write the post below the header in Markdown.
4. Commit and push. The site updates in about a minute.

A post with a date in the future does not show until that date.

## Keep a draft

Put unfinished posts in `drafts/`. That folder is excluded from the site,
but **it is still public on GitHub**, because the repo is public. Keep
anything you are not ready to reveal off this repo entirely.

## Add an image

Put the file in `assets/` and reference it as `/assets/name.png`.

## Change how the site looks

- Title, description, header links: `_config.yml`
- The About page: `about.md`
- The theme is `minima`, GitHub's plain built-in theme. Other built-in
  themes: https://pages.github.com/themes/

## First-time setup (once)

1. On GitHub, create a new **public** repo named `helix-0311.github.io`.
   Do not add a README (this folder already has its files).
2. In this folder:

   ```
   git add .
   git commit -m "Blog scaffold"
   git branch -M main
   git remote add origin https://github.com/helix-0311/helix-0311.github.io.git
   git push -u origin main
   ```

3. On GitHub: the repo's **Settings > Pages**. Under *Build and
   deployment*, set Source to **Deploy from a branch**, branch **main**,
   folder **/ (root)**. Save.
4. Wait a minute or two. The site is at https://helix-0311.github.io

If you name the repo something else (for example `devblog`), the address
is https://helix-0311.github.io/devblog and `_config.yml` needs
`baseurl: "/devblog"`.
