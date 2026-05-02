# IDA — Open Source Identity for the AI Age

Marketing site for **IDA**, the open-source identity platform.

This is a single-page static site (`index.html` + Google Fonts). No build step,
no framework. It deploys to Vercel as a static project.

## Live

- Site: https://adid.dev
- Docs: https://docs.adid.dev

## Local development

```sh
npm run dev
# → serves the site on http://localhost:3000
```

Or just open `index.html` in a browser. There is no build step.

## Deploy to Vercel

### One-click

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/myida/website)

### From the CLI

```sh
npm i -g vercel
vercel        # preview
vercel --prod # production
```

Vercel auto-detects this as a static project. Configuration lives in
[`vercel.json`](./vercel.json) and includes:

- `cleanUrls: true` — `/about.html` is served at `/about`
- Long-term cache headers for fonts and images
- Standard security headers (HSTS, `X-Content-Type-Options`, `Referrer-Policy`,
  `Permissions-Policy`, `X-Frame-Options`)

### Custom domain

Add `adid.dev` (or whatever domain you're using) under
**Project → Settings → Domains** in the Vercel dashboard.

## Project structure

```
.
├── index.html       # the entire site
├── vercel.json      # static hosting + headers config
├── package.json     # dev script only — no dependencies
├── LICENSE          # Apache 2.0
└── README.md
```

## Contributing

Issues and pull requests are welcome. By contributing you agree that your
contributions will be licensed under the Apache License 2.0.

## License

[Apache License 2.0](./LICENSE)
