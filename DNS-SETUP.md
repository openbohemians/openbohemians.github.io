# Open Bohemians custom domain setup

Host the existing static website on GitHub Pages and manage the domain's
DNS at Dynadot. Use `https://openbohemians.org/` as the canonical website
address, with `www.openbohemians.org` redirecting to it.

## DNS records

In Dynadot, open **My Domains → Manage Domains**, select
`openbohemians.org`, then **Action → DNS Settings → Dynadot DNS**.

| Section | Name | Type | Destination |
| --- | --- | --- | --- |
| Domain Record | Root domain; no name to enter | ANAME | `openbohemians.github.io` |
| Subdomain Records | `www` | CNAME | `openbohemians.github.io` |

Dynadot's Domain Record section represents the root domain; do not type
`@` into a subdomain field. Replace the current parking setup when applying
these records. Do not retain a conflicting root A, CNAME, forwarding, or
other website record alongside the ANAME. Preserve unrelated records if
any have been added since the inspection.

The ANAME record resolves GitHub's Pages addresses for the root domain.
If ANAME is unavailable in the account's interface, use these four root
A records instead: `185.199.108.153`, `185.199.109.153`,
`185.199.110.153`, and `185.199.111.153`. Use either ANAME or the A records.

## Deployment sequence

1. Have the Dynadot DNS entries ready to save. The website and domain
   settings must be changed together because the custom domain also affects
   project Pages sites without their own custom domains.
2. Publish the domain-change branch to `main`. Its root `CNAME` file contains
   `openbohemians.org`. Confirm repository **Settings → Pages → Custom domain**
   shows `openbohemians.org` before saving the DNS changes. If necessary,
   set the custom domain explicitly in Pages settings.
3. Save the DNS records above in Dynadot. Keep Dynadot as the DNS provider;
   no separate website hosting plan is needed for this static site.
4. Wait for DNS and GitHub's certificate provisioning. Confirm that the
   custom domain passes GitHub's DNS check and that **Enforce HTTPS** is enabled
   once the certificate is available.
5. Verify the home page, stylesheet, favicon, the `www` redirect, and the
   Oyl and Memo project sites. Update the organization's website field
   to `https://openbohemians.org/` after the custom domain is working.

DNS changes can take up to 24 hours to propagate. Check results rather
than treating elapsed time as proof of completion.

## Domain ownership verification

GitHub recommends verifying ownership before attaching a custom domain.
In the **Open Bohemians organization settings → Pages → Add a domain**,
add `openbohemians.org`. GitHub provides a unique TXT verification value
for `_github-pages-challenge-openbohemians.openbohemians.org`. Add that
value as a TXT subdomain record in Dynadot, verify it in GitHub, and keep
the TXT record. Use the actual value GitHub supplies.

## Inspection before setup

- Website: `https://openbohemians.github.io/`; Pages reports `built`, publishing
  `main:/`, with no custom domain configured.
- DNS provider: Dynadot, using `ns1.dyna-ns.net` and `ns2.dyna-ns.net`.
- Root A record: `185.53.179.128`.
- No MX or root TXT records, and no `www` CNAME, were returned by the initial
  DNS checks. These observations are a snapshot; recheck before changes.

## References

- [GitHub Pages custom domains](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site)
- [GitHub domain ownership verification](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/verifying-your-custom-domain-for-github-pages)
- [Dynadot DNS settings](https://www.dynadot.com/help/question/set-up-DNS)
