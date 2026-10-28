# bycuvola.com coming-soon page

Static HTML/CSS source lives in `site/`. No dependencies or build step.

Preview: `python3 -m http.server 4173 --directory site`

Vercel team: Cuvola (`team_4wFAHPOVnZUcGZ10HXmEfO8F`)
Project: bycuvola (`prj_qbjKjeqrTM1K3u93MzAqbBHo0baJ`)
Production: https://bycuvola.com
Vercel URL: https://bycuvola.vercel.app
Initial deployment: `dpl_Gzm38WGw2t5K8Quru61seRpZwAbd`

The initial deployment uploaded only the files inside `site/` through the Vercel connector. Git auto-deployment is not connected. For subsequent CLI deployment from the repository root, link to the existing bycuvola project in the Cuvola team, then use `vercel --prod`; root `vercel.json` sets the output to `site/`. Never deploy the internal brand documents as web content. Alternatively, connect this GitHub repository to the existing project from Vercel's Git settings; use no framework, no build command, and `site` as output directory.

DataFast's supplied script is in `site/index.html` head with website ID `dfid_zEE6lTGhj6PwnyCFSd2cP` and domain `bycuvola.com`. Browser markup was verified; dashboard event receipt was not inspected.

## Domain setup / rollback

Authoritative DNS is Cloudflare, zone `88018ef8f7d7ee27cc8bee24329df5de`.
Root A records: `216.198.79.1` and `64.29.17.1`, DNS only, TTL 300.
www CNAME: `7cfc984894729792.vercel-dns-017.com`, DNS only, TTL 300.
Vercel redirects www to apex with HTTP 308.

Previous parking records at apex were proxied A records `207.207.210.36`, `207.207.210.23`, and `207.207.210.50`, automatic TTL. Previous www was a proxied CNAME to `uixie.porkbun.com`, automatic TTL. These are the previous values if restoring parking is ever desired. The wildcard, MX, SPF, ACME TXT, and ricettario subdomain records were preserved.

## Verification (2026-10-28)

- Vercel deployment READY; domain configuration reports misconfigured=false.
- Production apex HTTPS returns HTTP 200 and renders the page in browser.
- Browser checked at desktop and 390px phone width; no horizontal overflow, artwork loads.
- Main CTA navigates to the story section.
- Exact supplied DataFast attributes present in head.
- Existing brand artwork adapted to an optimized JPEG; source is `/Users/cass/Cuvola/Cuvola Culinary Emblem (1).png`.
- Existing unrelated changes in branding/guidelines.md and .DS_Store left untouched.
