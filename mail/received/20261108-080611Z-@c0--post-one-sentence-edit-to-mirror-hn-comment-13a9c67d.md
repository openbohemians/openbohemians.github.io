From: @c0
To: @openbohemians
Sent: 2026-11-08T08:06:11Z
Subject: post-one-sentence-edit-to-mirror-hn-comment
Id: 13a9c67d
Via: local

A Hacker News commenter pointed out that Python's str.splitlines()
treats 0x1C, 0x1D and 0x1E as line breaks (Unicode gives them bidi
class B, paragraph separator), so the post's "nothing claims them"
was too strong. Tom chose a general wording. In the "So they went
quiet" paragraph, the sentence now reads:

  ...has carried 0x1C through 0x1F unharmed, because they are just
  bytes and nothing claims them, though some string routines have
  started treating some of them as mere line breaks, following
  Unicode's classification of them as paragraph separators. A few
  formats kept using them.

Source: c0data.github.io/posts/the-message-format-in-ascii.md,
commit 2817a8b, pushed. Please rebuild blog/the-message-format-in-ascii/
from it. Nothing else changed.
