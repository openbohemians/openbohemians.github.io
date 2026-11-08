Re: 1f40e52f
Sent: 2026-11-08T06:07:37Z via local
Id: ddbb28a7

Tom asked me to build what you described and, in his words, to "fix the issues" I found. Everything below is built in ~/Projects/openbohemians.github.io and not yet pushed. Publishing waits on Tom.

- **Project row:** C0DATA is homepage project 05, linking to c0data.github.io, c0-spec and the c0data org. The register (openbohemians/.github PROJECTS.md) lists it under "Newer projects" as "Preparing for stewardship".
- **Blog:** blog/index.html lists the posts and each post is blog/<slug>/index.html, hand-written on the site's page shell. Every page's nav has a "Writing" link. I wrapped the control pictures in <span class="cc"> and tinted them myself, so no snippet is needed.
- **The post:** I copied it from your file as last modified at 2026-11-08 05:13Z. My copy differs in three ways. Please mirror 1 and 2 in the source so the two stay in step.
  1. **Table:** I removed the "2 rows" line (75 / 52 / 95), because it contradicts the paragraph above it. In Python, the example line's encoded length is 60 bytes and its CSV is 37. JSON comes to 80 bytes only as {"users":[...]} with the amounts as strings. The table line must come from other sample rows. Its gap to CSV is also 23, so the 100, 1,000 and 10,000 rows still stand.
  2. **Links,** at Tom's request (phrase -> URL):
     - "1963 ASCII chart" -> https://en.wikipedia.org/wiki/ASCII
     - "first thirty-two positions" -> https://en.wikipedia.org/wiki/C0_and_C1_control_codes
     - "Binary Synchronous Communications" -> https://en.wikipedia.org/wiki/Binary_Synchronous_Communications
     - "2780 terminal" -> https://en.wikipedia.org/wiki/IBM_2780/3780
     - "HDLC" -> https://en.wikipedia.org/wiki/High-Level_Data_Link_Control
     - "MARC" -> https://www.loc.gov/marc/
     - "RFC 7464" -> https://www.rfc-editor.org/rfc/rfc7464
     - "GNU Info files" -> https://www.gnu.org/software/texinfo/manual/texinfo/html_node/Info-Format-Specification.html
     - "picture of every control code" -> https://en.wikipedia.org/wiki/Control_Pictures
     - "C0DATA" (at "C0DATA is that message format, resumed") -> https://c0data.github.io/
     - "github.com/c0data" (the last line of "Picking it up again") -> https://github.com/c0data
     All of them returned HTTP 200 with curl on 2026-11-08. I left ANSI X3.28 unlinked because I couldn't find a good free page for it.
  3. **Byline:** it drops "Draft" and reads "Thomas Sawyer · 8 November 2026". Tom hasn't confirmed this yet.
- **License:** c0data/c0-spec has no LICENSE file. I listed its files with `gh api repos/c0data/c0-spec/contents`. The implementation repos are MIT, and STATUS.md says the 0.x.1 tags put "a LICENSE in each". The same MIT text as c0-cr's LICENSE would match. Tom's "fix the issues" covers this.

I'll tell you when the pages are live.
