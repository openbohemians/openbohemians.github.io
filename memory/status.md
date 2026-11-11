# Status

*Updated 2026-11-11*

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
- **Blog engine, the user's decision (2026-11-08):** "I am not writing blog
  posts in html. we need a blog engine." The blog is now Jekyll, which
  GitHub Pages builds from `main` (website `743a7ef`). Posts are Markdown in
  `_posts/YYYY-MM-DD-slug.md`, published at `/blog/slug/`. The layouts are
  `_layouts/default.html` and `post.html`, and `blog/index.html` lists the
  posts from `site.posts`. The homepage and support letter have no front
  matter, so they're copied unchanged. The README says how to write a post.
  At the user's prompting, posts and layouts moved into `blog/_posts/` and
  `blog/_layouts/` (`layouts_dir`), and only `_config.yml` stays at the top
  (`25ae31d`, which builds byte-for-byte the same site). **Not yet
  pushed.**
  A post from @c0 is its markdown source with the title and byline lines
  swapped for front matter. Every page's nav has a "Writing" link, and on
  phones the nav is a grid of two rows of three.
- **First post:** "The message format that was already in ASCII". The
  control pictures (U+2400–U+2426) are wrapped in `<span class="cc">` and
  tinted with the accent colour. The post layout does this with a Liquid
  loop, since GitHub Pages runs no custom plugins.
- **Keeping the copies in step:** @c0 asked to be told when a post is
  copied. If the author edits the source, the page needs updating. The
  published page drops the source's "Draft" label, which the user approved.
- **Fixes the user asked for ("fix the issues", 2026-11-08):** in our copy,
  the table's two-row line (75 / 52 / 95) is gone, because it contradicted
  the 60-byte example. 11 links were also added at the user's request. All
  of this went to @c0 to mirror in the source, along with a request to add
  an MIT LICENSE to `c0data/c0-spec`
  (`mail/sent/20261108-060736Z-@c0--…`). **Done by @c0:** the source took
  the table fix, the links and the byline (c0data.github.io `784a60a`,
  `2bc50d0`), and c0-spec got its LICENSE (`e94ae62`). @c0 also fixed the
  1967 ESC slip itself ("The first four became CAN, EM, SUB, ESC") and
  rewrote the transparent-mode passage.
- **Synced 2026-11-08 (website `737f4b7`):** our copy was rebuilt from the
  source as of 06:33Z. It adds one sentence the user approved, saying that
  c0fmt converts between compact and pictured form and the VS Code
  extension highlights the pictures and aligns columns. That was checked
  against the c0-fmt and c0-ed READMEs. The source doesn't have this
  sentence yet.
- **One copy, on openbohemians.org:** the user decided on 2026-11-08 (as
  relayed by @c0, `mail/received/…-219fc1eb.md`) that project blog posts
  live only on openbohemians.org, and project sites just list them with
  links. c0data.github.io's Writing page now links to our posts, and its
  old copies at `/posts/<slug>/` redirect here (meta refresh plus a
  canonical link to ours, checked with curl on 2026-11-11). The markdown
  sources stay in `c0data.github.io/posts/*.md`, where @c0 writes them.
  @c0 sends each new post as markdown with a one- or two-sentence summary,
  and we swap its title and byline lines for front matter. It accepted the
  summary written for "Reading the chart again" (`…-07994ebf.md`). Nothing
  is open between us.
- **Hacker News:** the user cleared the post for HN on 2026-11-08, leaving
  the quality call to this agent, which judged it ready. @loudly has the
  details (`mail/sent/…@loudly--hn-…`). Tom submits it himself, as an
  ordinary link rather than Show HN.
- **After HN, 2026-11-08:** a commenter pointed out that Python's
  `str.splitlines()` treats FS, GS and RS as line breaks, because Unicode
  classes them as paragraph separators. That made "nothing claims them"
  too strong. The user chose a general wording, and @c0 put it in the
  source (`2817a8b`). Our copy was rebuilt from that source, and the
  sentence is the only change (website `743a7ef`).
- **Second post, "Reading the chart again":** approved by the user (as
  relayed by @c0, `mail/received/…-ceca6950.md`). Built from c0data.github.io
  `bd81fe4` at `blog/reading-the-chart-again/` and listed first on the
  Writing page (website `743a7ef`). @c0's copy's canonical link already
  points here. Jekyll's output for both posts was checked block by block
  against the hand-built pages it replaced, and matches. **Live and
  checked 2026-11-08:** the Pages run was green, and the live pages match
  the hand-built ones block by block, meta tags included. @c0 has been told
  (`mail/sent/20261108-190721Z-@c0--…`). It keeps sending markdown, with an
  optional summary for the Writing page.

## Open

- **Register:** Memo and March still wait for a stewardship review.
- **Status:** no project is "Maintained" yet. Admission is the user's
  decision as founding steward.
