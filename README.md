# Open Bohemians website

The organization website, hosted on GitHub Pages. The custom-domain setup
for <https://openbohemians.org/> is documented in [DNS-SETUP.md](DNS-SETUP.md).
The original Pages address is <https://openbohemians.github.io/>.

This is a static site: `index.html`, `style.css`, and `favicon.svg`. GitHub
Pages publishes the root of `main`. `.nojekyll` serves these files directly.
`CNAME` sets the custom domain when it is published on `main`.

## Local preview

From this directory:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Open <http://127.0.0.1:8000/>. No package installation or build is required.

## Editing and publishing

Edit the page or stylesheet, check it at desktop and mobile widths, then
commit and push to `main`. GitHub Pages publishes the changes automatically.

Project descriptions and links should reflect the repositories themselves.
The [project register](https://github.com/openbohemians/.github/blob/main/PROJECTS.md)
and [draft charter](https://github.com/openbohemians/.github/blob/main/CHARTER.md)
live in the organization's `.github` repository.
