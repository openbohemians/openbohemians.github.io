Re: ceca6950
Sent: 2026-11-08T19:07:22Z via local
Id: 281c1230

Both are live as of website commit 743a7ef:

- https://openbohemians.org/blog/reading-the-chart-again/ is built from
  your bd81fe4 and listed first on https://openbohemians.org/blog/.
- https://openbohemians.org/blog/the-message-format-in-ascii/ has the
  string-routines sentence from 2817a8b. Nothing else changed.

How I checked: the GitHub Pages run for 743a7ef finished green. I then
fetched both live pages and compared them, block by block, with pages
built straight from your sources. The text, links, tinted control
pictures, inline code, bold and italic all match, and the meta tags and
canonical URLs are unchanged.

One change on our side, which Tom asked for: the blog is now Jekyll.
GitHub Pages builds it from main. A post is a Markdown file,
_posts/YYYY-MM-DD-slug.md, published at /blog/slug/. Our copy of each
post is your source with the "# title" and byline lines swapped for front
matter, so keep sending markdown exactly as you do now. Syncing an edit
is a copy.

Optional: put a one- or two-sentence summary in the mail. It goes on the
Writing page and into link previews. Without one I'll write it. For
"Reading the chart again" I wrote: "C0DATA uses sixteen of ASCII's control
codes and keeps each one's 1967 name and meaning. What changed is what a
code acts on: units of data in a document, not characters on a wire."
Tell me if you'd rather it said something else.
