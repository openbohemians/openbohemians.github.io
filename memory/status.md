# Status

*Updated 2026-11-08*

## What this project covers

- **Website** (this repo, published at openbohemians.org from `main` by
  GitHub Pages): the homepage (`index.html`) and the founder's support
  letter (`support/index.html`). A push to `main` is live in about 20
  seconds.
- **Org `.github` repo** (`openbohemians/.github`): the org profile
  (`profile/README.md`, shown at github.com/openbohemians), the project
  register (`PROJECTS.md`), and the Sponsors copy (`sponsors/introduction.md`,
  `sponsors/short-bio.txt`).
- **The Sponsors page doesn't update from the repo.** The user pastes the
  introduction and short bio into the Sponsors dashboard by hand. The files
  record what's live.

## Rule: keep the project list in one place

The user decided this on 2026-11-07. The homepage's `#projects` section and
the register are the only places that list the projects. Other copy (the
Sponsors introduction and bio, the org profile, the homepage Sponsor
section) links to the homepage rather than naming projects. Every extra
list is one more thing to keep up to date. The Oyl bindings are written as
"its bindings" for the same reason.

The support letter's "The work includes…" sentence is the accepted
exception, because it doesn't claim to be complete. When a project is
added, ask whether it belongs there.

This is settled, so it could go in the website README. That hasn't been
done.

## Done, 2026-11-07 to 2026-11-08

- **Support letter:** a new opening, Jargon named, "Paid development
  requests" became "Hire me" (any software project, and employment), and
  the title keeps "Open Bohemians" together with only the name in red.
  Website commits `1b7cba9` and `f04cdb9`.
- **Homepage:** Jargon added as project 03, Merkle CHAMP moved to 04, and
  the project names removed from the Sponsor section (`1b7cba9`, `f0028aa`).
- **Register:** added Jargon and Merkle CHAMP under "Newer projects", both
  "Preparing for stewardship". The user said they "both work well, if
  still a bit new". Also added Oyl's Rust and Go bindings (`.github`
  `22a4c79`).
- **Sponsors copy:** project names removed, and the bio is now "Open
  Bohemians: a home for open source software, maintained with care." The
  user changed it on the live page (`.github` `4237764`).
- **Org profile and `.github` README:** Oyl is described as having "its
  bindings" (`.github` `37805b8`).

## C0DATA and the blog, 2026-11-08

- **The decision:** C0DATA is an Open Bohemians project, and its blog posts
  are published on openbohemians.org, with a copy kept in c0data's own site
  repo. @c0 relayed this as the user's decision
  (`mail/received/…@c0--c0data-project-row-blog-directory-first-post-1f40e52f.md`).
  The user confirmed it here by passing the work to this agent.
- **Published 2026-11-08:** C0DATA as homepage project 05, a C0DATA row in
  the register, and C0DATA in the support letter's "The work includes…"
  sentence, all approved by the user.
- **Blog:** hand-written static pages with no generator. `blog/index.html`
  lists the posts, each post is `blog/<slug>/index.html`, and every page's
  nav has a "Writing" link. On phones the nav is a grid of two rows of
  three.
- **First post:** "The message format that was already in ASCII", converted
  from @c0's markdown with a one-off script. The control pictures
  (U+2400–U+2426) in code blocks are wrapped in `<span class="cc">` and
  tinted with the accent colour.
- **Keeping the copies in step:** @c0 asked to be told when a post is
  copied. If the author edits the source, the page needs updating. The
  published page drops the source's "Draft" label, which the user approved.
- **Fixes the user asked for ("fix the issues", 2026-11-08):** in our copy,
  the table's two-row line (75 / 52 / 95) is gone, because it contradicted
  the 60-byte example. 11 links were also added at the user's request. All
  of this went to @c0 to mirror in the source, along with a request to add
  an MIT LICENSE to `c0data/c0-spec`
  (`mail/sent/20261108-060736Z-@c0--…`). **Open** until @c0 confirms.

## Open

- **Register:** Memo and March still wait for a stewardship review.
- **Status:** no project is "Maintained" yet. Admission is the user's
  decision as founding steward.
