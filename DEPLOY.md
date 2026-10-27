# Publishing the portfolio on GitHub Pages

This portfolio is separate from the ZAQ Media website and the ZAQ resume. It lives in its own repository, `zaq-portfolio`, and uses GitHub's free address. No custom domain is needed.

## 1. Create the repository

1. On github.com, click **+ → New repository**.
2. Name it `zaq-portfolio`, set it to **Public**, and leave "Add a README" unticked.
3. Click **Create repository**.

## 2. Upload the files

1. On the new repository page, click **uploading an existing file**.
2. Drag in everything inside this folder: `index.html`, the `media` folder, `robots.txt`, `sitemap.xml`, `README.md`, `DEPLOY.md`, `.gitignore`.
3. Click **Commit changes**.

## 3. Turn on GitHub Pages

1. In the repository, go to **Settings → Pages**.
2. Under **Build and deployment**, set **Source** to "Deploy from a branch", **Branch** to `main` and folder `/ (root)`. Save.
3. After a minute the portfolio is live at `https://<your-username>.github.io/zaq-portfolio/`.

## 4. Let Vimeo play there

For each video on vimeo.com: **Settings → Privacy → Where can this be embedded?** → **Specific domains**, and add `<your-username>.github.io`.

Leave **Settings → Pages → Custom domain** empty, and don't add a `CNAME` file to the repo.
