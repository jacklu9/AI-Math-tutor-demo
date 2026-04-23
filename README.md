# AI Math Tutor

This folder is a clean, internet-deployable copy of the local website from `/Users/zijielu/gemini-test/webtest_copy`.

## What the site does

It is a frontend-only Vite + React app for a guided math tutoring demo. The site lets a user:

- paste a math problem
- preview and analyze the problem structure
- choose a help mode such as explanation, method choice, worked example, staged answer, or fixing mistakes
- read math-rendered tutor guidance with KaTeX

There is no backend or database. Everything is currently demo content rendered in the browser.

## Project structure

- `src/App.jsx`: main multi-step tutor interface
- `src/main.jsx`: React entry point
- `src/index.css`: Tailwind entry styles
- `index.html`: app shell
- `dist/`: static build output that can be uploaded directly to a static host

## Run locally

```bash
npm install
npm run dev
```

## Build

```bash
npm run build
```

## Put it on the internet

This project is ready for static hosting. You can deploy it with:

- Vercel: import this folder as a Vite project
- Netlify: import this folder, build command `npm run build`, publish directory `dist`
- GitHub Pages / Cloudflare Pages / any static host: upload the contents of `dist/`

## GitHub Pages

This folder now includes a GitHub Actions workflow at `.github/workflows/deploy.yml` that deploys automatically to GitHub Pages when you push to the `main` branch.

To publish it:

1. Create a GitHub repository.
2. Upload the contents of this folder to that repository.
3. In GitHub, open `Settings > Pages`.
4. Set the source to `GitHub Actions`.
5. Push to `main`.

The Vite config automatically uses the correct GitHub Pages base path during the GitHub Actions build, so assets load from `/<repo-name>/` when deployed.

## Notes

- I removed the unused `/vite.svg` favicon reference so the deployed site does not request a missing file.
- A prebuilt `dist/` copy is included for direct upload.
