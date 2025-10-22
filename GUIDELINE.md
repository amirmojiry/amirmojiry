## Working With This Jekyll Site

The repository is now a Jekyll project that uses the Cayman theme out of the box. Follow the steps below to preview, customize, and publish updates.

### 1. Local setup

```bash
gem install bundler # only needed once
bundle install
bundle exec jekyll serve
```

Visit `http://127.0.0.1:4000/` (or the URL printed in the terminal) to see the site. Jekyll rebuilds automatically when you edit files.

### 2. Updating site-wide settings

- `_config.yml` holds metadata such as the site title, description, navigation, and GitHub username.
- Set `url` and (optionally) `baseurl` before publishing so canonical links are correct. For a project site like `https://amirMojiri.github.io/amirMojiri/`, set `baseurl: "/amirMojiri"`.
- The Cayman theme comes from GitHub Pages, so no extra theme files are needed.

### 3. Editing the main pages

- `index.md` — landing page with the quick intro, featured app, latest post snippet, and contact links.
- `apps/index.md` — catalog view that links out to each app.
- `apps/<app-slug>/index.md` — app overview template. Duplicate the `sample-app` folder for new products.
- `apps/<app-slug>/privacy.md` — privacy policy per app. Keep the permalink structure the same so links stay predictable.
- `blog/index.md` — blog landing page. It lists all posts automatically.

Every file begins with YAML front matter to tell Jekyll which layout to use and what URL to generate.

### 4. Publishing a blog post

1. Copy `_posts/2024-01-01-hello-world.md`.
2. Rename it to `YYYY-MM-DD-descriptive-title.md`.
3. Update the `title`, `date`, and body content.
4. Push the changes — the blog index and RSS feed update automatically.

### 5. Adding a new app

1. Duplicate `apps/sample-app`.
2. Rename the folder to the app slug (no spaces, lowercase recommended).
3. Edit the new `index.md` with the intro, download links, and feature list.
4. Replace `privacy.md` with your real policy.
5. Add links to `apps/index.md` (and optionally `index.md` for a featured slot).

### 6. Deploying on GitHub Pages

1. Push the repository to GitHub.
2. Open **Settings → Pages**.
3. Set the source to the `main` branch and the `/ (root)` directory.
4. Save — GitHub builds the site automatically using the bundled Cayman theme.
5. Use the published URL in the repository settings for easy sharing.

### 7. Optional enhancements

- Override styles by creating `assets/css/style.scss` with front matter and custom rules.
- Add plugins (e.g. `jekyll-sitemap`) by listing them in `_config.yml` under `plugins`.
- Incorporate structured data or SEO tweaks via `_includes` if you need more control.
