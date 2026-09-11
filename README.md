# Photo Editor

Photo Editor is a browser-only image uploader that previews JPEG or PNG files with selectable Instagram-style CSS filters.

## Core features

- Local JPEG and PNG file selection.
- In-browser preview using an object URL; the selected file is not uploaded by this code.
- A selectable catalog of Instagram-style CSS filters.
- Client-side JPEG download using Canvas and FileSaver.
- Two-page React Router flow for the landing page and editor.

## Technology stack

- React 18 and React Router 6
- Vite 5
- JavaScript/JSX and Tailwind CSS 3
- `instagram.css` filter classes
- Browser Canvas APIs and FileSaver.js

## Prerequisites

- Node.js compatible with the locked dependencies
- npm
- A modern browser with Canvas, Blob, and object-URL support

## Local setup

```bash
git clone https://github.com/varunisrani/photo-editor.git
cd photo-editor
npm ci
npm run dev
```

Build and inspect the production bundle with:

```bash
npm run build
npm run preview
```

Lint the project with `npm run lint`.

## Configuration

No environment variables are referenced by the current application.

## Project structure

- `src/main.jsx` — application entry point
- `src/components/Oranganisms/Approute.jsx` — landing and editor routes
- `src/components/Oranganisms/Home.jsx` — landing page
- `src/components/Oranganisms/File.jsx` — file selection, filter preview, and download
- `src/components/Oranganisms/instagram*.css` — bundled filter styles

## Status and limitations

This is a client-side prototype. The selected CSS filter affects the preview, but the download routine redraws the original image onto Canvas without applying that CSS filter, so the saved JPEG may not match the filtered preview. There are no crop, resize, undo, persistence, or server-upload workflows in the active routes.
