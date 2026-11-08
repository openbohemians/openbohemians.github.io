# Open Bohemians website

The organization website, hosted on GitHub Pages. The custom-domain setup
for <https://openbohemians.org/> is documented in [DNS-SETUP.md](DNS-SETUP.md).
The original Pages address is <https://openbohemians.github.io/>.

GitHub Pages builds the site with Jekyll from the root of `main`. The
homepage (`index.html`) and the founder’s support letter (`support/index.html`)
are plain HTML with no front matter, so Jekyll copies them as they are.
`CNAME` sets the custom domain when it is published on `main`.

## Writing a post

Posts are Markdown files in `_posts/`, named `YYYY-MM-DD-slug.md`. Each is
published at `/blog/slug/`, and the Writing page (`blog/index.html`) lists
them, newest first. Start a post with:

```markdown
---
title: "The post's title"
date: 2026-11-08 16:30:00 +0000
description: "One or two sentences for the Writing page and link previews."
project: C0DATA                       # optional: shown in the eyebrow
project_url: https://c0data.github.io/  # optional: the "About" link
---

The first paragraph...
```

The author defaults to Thomas Sawyer; add `author:` to change it. The date
and time order posts published on the same day. Control Pictures
(U+2400–U+2426, such as ␞ and ␟) are tinted wherever they appear. The page
layout is in `_layouts/`: `default.html` is the shell, `post.html` the post.

## Local preview

From this directory, with Jekyll installed (`gem install jekyll kramdown-parser-gfm`):

```sh
jekyll serve
```

Open <http://127.0.0.1:4000/>.

## Editing and publishing

Edit the page or stylesheet, check it at desktop and mobile widths, then
commit and push to `main`. GitHub Pages publishes the changes automatically.

Project descriptions and links should reflect the repositories themselves.
The [project register](https://github.com/openbohemians/.github/blob/main/PROJECTS.md)
and [draft charter](https://github.com/openbohemians/.github/blob/main/CHARTER.md)
live in the organization's `.github` repository.
