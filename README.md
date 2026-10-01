# Vanessa Williams — GitHub Pages portfolio

A static, self-contained version of your CV website. Includes the interactive career timeline, expandable skills, volunteering and projects page, Yokaruna branding and shop links, local fonts, artwork and downloadable CV. No upload controls, database, server or build tools are required.

## Deploy using the GitHub website

1. Sign in to https://github.com and create a new repository named `vanessa-portfolio`. Choose Public for GitHub Free. If you prefer your main profile URL, name it `YOUR-USERNAME.github.io` instead.
2. Extract the downloaded ZIP on your computer.
3. In the repository, choose **Add file → Upload files**. Upload the CONTENTS of the extracted `vanessa-github-pages` folder, including the `assets` folder. Do not upload the ZIP itself or wrap the files in an extra folder. `index.html` must be at the repository root.
4. Commit the files to the `main` branch. If your file browser hides `.nojekyll`, create it through **Add file → Create new file**, name it `.nojekyll`, and commit it (a comment or empty file is fine).
5. Go to **Settings → Pages**. Under **Build and deployment**, choose **Deploy from a branch**.
6. Select branch **main**, folder **/(root)**, then click **Save**.
7. Wait for the Pages deployment to finish. Check the **Actions** tab if needed. **Settings → Pages** will show your published URL.

For a repository called `vanessa-portfolio`, your URL is `https://YOUR-USERNAME.github.io/vanessa-portfolio/`. For a repository called `YOUR-USERNAME.github.io`, it is `https://YOUR-USERNAME.github.io/`.

## Deploy using Git (optional)

Create an empty GitHub repository first, then run these commands from inside the extracted folder. Replace YOUR-USERNAME with your GitHub username.

```bash
git init
git add .
git commit -m "Add portfolio website"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/vanessa-portfolio.git
git push -u origin main
```

Then configure **Settings → Pages → Deploy from a branch → main → /(root)** as above.

## Preview locally

Open `index.html` in your browser, or run `python -m http.server 8000` inside this folder and visit http://localhost:8000/ . The community page is `community.html`.

## Edit your content

- `script.js`: career roles, skills, certification details and community project text. Both HTML pages use this shared file.
- `styles.css`: colours, typography, layout, responsive styles and motion.
- `index.html` and `community.html`: page titles, navigation, contact footer and metadata. Update shared navigation/footer in both files.
- `cv.pdf`: replace this file to update the downloadable CV, keeping the same filename.
- `assets/yokaruna-pattern.png`: replace to update the patterned artwork, keeping the same filename.
- `assets/`: local Bayon and Chivo fonts, copied from your shop's font resources. Keep any applicable font licensing conditions when redistributing.

To add your own image to a community project, add a file to `assets/` and insert an image element in that project's markup in `script.js`, using a relative URL such as `./assets/art-market.jpg`. There is no visitor upload page.

After committing edits to `main`, GitHub Pages republishes the site automatically.

## Public content

GitHub Pages publishes a publicly accessible site. This package contains your contact email and the original CV PDF, including its phone number. Review or replace `cv.pdf` if you want different contact details on your public site. Your shop remains at https://yokaruna.com — this package does not change its domain or hosting.

## Troubleshooting

- Blank page or missing styles: ensure `index.html`, `script.js`, `styles.css` and `assets/` are at the repository root, not inside an extra folder.
- Missing volunteering page: ensure `community.html` is uploaded with that exact lowercase name.
- 404 immediately after setup: wait for the deployment to complete and use the URL shown in Settings → Pages.
- No Pages build: check that GitHub Actions is enabled and the selected branch is `main`.
- Old content after an update: check the Actions deployment, then refresh your browser cache.

## Official guidance

https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site
https://docs.github.com/en/pages/quickstart
