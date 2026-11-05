# Anxious Bean Studios — Website Starter

A responsive, static developer-studio website with a built-in JSON-powered devlog. No paid hosting or database required.

## Preview locally

From the folder containing `index.html`, run:

```bash
python -m http.server 8000
```

Open `http://localhost:8000`. Opening `index.html` directly as a file will not load JSON posts because browsers restrict local fetch requests.

## Publish on GitHub Pages

1. Create a GitHub repository, e.g. `anxious-bean-studios`.
2. Upload the **contents** of this folder to the repository root.
3. In the repository, go to **Settings → Pages**.
4. Choose **Deploy from a branch**, select `main` and `/ (root)`, then save.
5. GitHub will provide a public `github.io` website address. You can connect a custom domain later.

## Publish a new devlog entry

1. Open `posts.json` in GitHub and click the pencil/edit icon.
2. Add another object to the JSON array (separated by a comma). Example:

```json
{
  "id": "new-washers",
  "date": "2026-11-12",
  "category": "DEVELOPMENT UPDATE",
  "title": "The Washers Got an Upgrade",
  "excerpt": "A quick look at the latest machine improvements.",
  "body": [
    "First paragraph of your update.",
    "Second paragraph with more detail."
  ]
}
```

3. Commit the change. The website updates automatically after GitHub Pages deploys it. Posts appear newest first and have shareable links like `?post=new-washers#post-detail`.
4. **Important:** JSON requires double quotes and commas between objects. Check the format before committing.

## Steam link

Edit `site-config.json` and set `steamUrl` to the real store page URL when available. Until then, the site uses a placeholder, not a fake store link.

## Screenshots

Replace the three gallery placeholders in `index.html` with real game screenshots (`<img src="assets/your-image.png" alt="...">`) and add image styling in CSS as needed. The current illustrations are decorative CSS, not game screenshots.

## Customize

- `index.html` — content and sections
- `assets/style.css` — colors, layout, typography
- `assets/app.js` — devlog rendering and navigation
- `posts.json` — devlog posts
- `site-config.json` — Steam URL

The included first devlog is explicitly marked **DRAFT** and should be reviewed before public launch. No release date, developer identity, or Steam page has been invented.
