# Profile Page — Prince

This is a simple static profile page created for Prince.

Files:
- `index.html` — the main page with bio, skills, and image.
- `styles.css` — styles used by the page.
- `assets/profile.svg` — placeholder image (replace with your real photo).

How to use:
1. Open `index.html` in your browser (double-click or open from VS Code Live Server).
2. To add your real photo, replace `assets/profile.svg` with your `jpg`/`png` file and keep the same filename, or edit the `<img>` src in `index.html`.
3. Edit the text in `index.html` to add more details about yourself (projects, links, contact info).

Notes:
- The content includes bilingual lines (English + Hindi/romanized) as you wrote them; feel free to edit.
- If you want, I can add sections for Projects, Education timeline, or export this to a PDF/profile-card. Tell me what you'd like next.

## Deploying to GitHub + CI/CD (automatic deploy on push)

This project can be deployed to GitHub Pages and set up to auto-deploy on every push to the `main` branch using GitHub Actions. I added a workflow at `.github/workflows/deploy.yml` that:

- Runs on `push` to `main`.
- Uploads the repository contents as a Pages artifact and deploys with the official `actions/deploy-pages` action.

Quick steps to enable deployment from your machine (PowerShell commands):

1. Initialize git (if you haven't already), commit and push to GitHub:

```powershell
cd "c:\Users\lucky\OneDrive\Pictures\Desktop\story\profile_page"
git init
git add -A
git commit -m "Initial profile page"
# Create repository on GitHub (use GitHub website or gh CLI), then push:
# replace <USERNAME> and <REPO> with your values
git branch -M main
git remote add origin https://github.com/<USERNAME>/<REPO>.git
git push -u origin main
```

2. In the repository Settings → Pages, set the source to "GitHub Actions" (the workflow will deploy automatically). Modern repos can keep default Pages settings — the workflow will publish to GitHub Pages.

Notes & troubleshooting:
- The workflow uses the official Pages actions and requires no extra secrets. Make sure GitHub Pages is allowed in your repository and that the `main` branch is the branch you push to.
- If your default branch is `master` or a different name, change the `on.push.branches` value in `.github/workflows/deploy.yml`.
- If you want a custom domain or HTTPS, configure it in the Pages settings.

If you'd like, I can:
- Create a `CNAME` file for a custom domain.
- Add a small build step (e.g., run a static site generator or minifier) before deployment.
- Configure the repository for a public GitHub Pages site with a CI badge in the README.

Tell me which GitHub repo name you want (or paste the repo URL) and I can update the README with exact push commands and set the workflow branch if you use a different default branch.