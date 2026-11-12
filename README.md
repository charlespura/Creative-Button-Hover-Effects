# Button Lab

A React + TypeScript playground for creative button hover effects, built with Vite. Designed in navy blue, cool grey, and crisp white.

## Features

- 16 live effects, including all eight original effects: Neon Glow, Sliding Borders, Morphing Shape, Shadow Expansion, Underline Sweep, Gradient Pulse, Ripple Effect, and Flip Effect.
- Search by name and filter by Essentials, Motion, Glow & color, or Borders.
- Hover a card to preview its effect; click the actual button for live feedback. Buttons also work with keyboard focus and touch.
- View React, HTML, and standalone CSS snippets. Copy a snippet or the complete React + CSS example.
- Responsive layout, visible focus indicators, native accessible code dialog, and reduced motion support.

## Run locally

Requires Node.js 22 and npm.

```sh
npm ci
npm run dev
```

Open the local URL printed by Vite. This project uses Vite; opening index.html directly or serving the source through XAMPP will not compile TypeScript.

```sh
npm run build
npm run preview
```

The build performs a TypeScript check and writes the production site to `dist/`.

## Use a button

1. Choose an effect and select **View code**.
2. Copy the React component into your project (or select HTML for a plain HTML project).
3. Copy the CSS into `button.css` alongside the component. The React snippet imports this file.
4. Replace the example click handler with your own action.

**Copy code** on a card copies both React and CSS in one text block; place the component and CSS in their respective files. Clipboard access requires HTTPS or localhost. If clipboard access is unavailable, open View code and select the text manually. Effects use a shared `.button` selector in copied examples; rename it if combining multiple styles on one page.

## Deploy to GitHub Pages

1. Push this project, including `package-lock.json`, to your GitHub repository on `main` or `master`.
2. Open **Settings ? Pages ? Build and deployment** and select **GitHub Actions** as the source.
3. The workflow in `.github/workflows/deploy.yml` builds and deploys on each push. You can also run it from **Actions ? Deploy to GitHub Pages ? Run workflow**.
4. Find the published URL in the workflow's deployment output or repository Pages settings.

Vite uses a relative asset base (`./`), so the build works at both a repository subpath and a custom domain. If your default branch has a different name, update the workflow's branch list. Deployment requires Pages to be available and enabled for the repository.

## Project layout

- `src/App.tsx` — gallery, filters, interactive feedback, and code dialog
- `src/effects.ts` — typed effect catalog and standalone code generation
- `src/styles.css` — responsive gallery theme
- `vite.config.ts` — React and deployment asset configuration
- `.github/workflows/deploy.yml` — GitHub Pages build and deployment

The app has no component library or animation dependencies. Google Fonts enhance typography when available; local system fonts provide a fallback.

Created by Charles Pura.
