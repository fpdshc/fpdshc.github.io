# fpdshc.github.io

The organization root website for **Faculty Professional Development Services (FPDS)** at Hillsborough College, served by GitHub Pages at <https://fpdshc.github.io/>.

## What this repository is

GitHub serves an organization's root site from the repository named exactly `<organization>.github.io`. This repository exists so that <https://fpdshc.github.io/> resolves to a root website rather than returning 404, and so that this domain can be crawled and cited cleanly.

The root page redirects to the canonical index of FPDS apps and resources at <https://fpdshc.github.io/apps/>, which lives in the [apps](https://github.com/fpdshc/apps) repository.

## Files

- `index.html` — the root page. Redirects to `/apps/` by meta refresh and by script, with a visible link as a fallback for anyone whose browser blocks either. Carries a canonical URL pointing at `/apps/` and schema.org `Organization` metadata, so crawlers consolidate the two URLs rather than treating the redirect as duplicate content.
- `robots.txt` — allows every user agent, and names AI crawlers and assistants explicitly (GPTBot, OAI-SearchBot, ClaudeBot, PerplexityBot, Google-Extended, CCBot, and others), plus a `Sitemap:` line.
- `sitemap.xml` — every page that currently resolves on this domain.
- `llms.txt` — a plain-text index of the FPDS resources, written to be read by AI agents and assistants as well as people.
- `.nojekyll` — tells GitHub Pages to publish the files as they are, with no Jekyll processing.

## Adding files

There is no build step. Any static file committed here is published as-is, so the repository can stay minimal.

If a full site is ever wanted at the domain root rather than a redirect, replace `index.html` with that site and update `sitemap.xml` and `llms.txt` to match.

## Related

- [apps](https://github.com/fpdshc/apps) — the educational apps and resources themselves, published at <https://fpdshc.github.io/apps/>.