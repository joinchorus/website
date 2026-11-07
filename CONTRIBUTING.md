# Contributing to the Chorus website

This repository is the source of [joinchorus.app](https://joinchorus.app), the manifesto page for [Chorus](https://github.com/joinchorus/chorus). Changes to the application itself belong in [joinchorus/chorus](https://github.com/joinchorus/chorus) and follow the [organization contributing guide](https://github.com/joinchorus/.github/blob/main/CONTRIBUTING.md).

## Run it locally

The site is a single static HTML page with inline CSS; there is no build step.

```bash
git clone https://github.com/YOUR_USERNAME/website.git
cd website
npm run serve        # npx serve public, prints the local address (default http://localhost:3000)
```

Requirements: Node.js 22 or newer (only for `npx serve`).

## Where things live

| Path | Content |
| :--- | :--- |
| `public/index.html` | The whole page, including its CSS and theme toggle |
| `public/logo.svg`, `public/favicon.svg` | Brand mark |
| `public/robots.txt`, `public/sitemap.xml` | Crawling metadata |
| `firebase.json` | Firebase Hosting configuration |

## Writing for the site

- Chorus is in early development (v0.1.0-alpha). Do not describe features that are not in the app, and do not add metrics or testimonials.
- Keep the page fast and self-contained: no trackers, no remote fonts, no new third-party scripts.
- Check both light and dark themes and a narrow (mobile) viewport before opening a pull request.

## Pull requests

1. Branch from `main` (`docs/...`, `fix/...`, `feat/...`).
2. Use [Conventional Commits](https://www.conventionalcommits.org/) (`fix: correct footer link`).
3. Open a pull request using the template. CI checks that `public/index.html` is present; a maintainer review is required.
4. **Merging to `main` deploys to joinchorus.app**, so preview your change locally first.

Security issues: please do not open a public issue. Use [private vulnerability reporting](https://github.com/joinchorus/website/security/advisories/new) or see the [security policy](https://github.com/joinchorus/.github/blob/main/SECURITY.md).
