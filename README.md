# Don Fournier — Portfolio Site

A self-contained, single-page portfolio (no build step, no dependencies) ready for **GitHub Pages**.

```
portfolio-site/
├── index.html                     # the whole site (HTML + CSS + a few lines of JS)
├── assets/
│   └── Don_Fournier_Resume.pdf    # linked by the "Résumé" buttons
├── .nojekyll                      # tells GitHub Pages to serve files as-is
├── .gitignore
└── README.md
```

## Preview locally
Just open `index.html` in a browser (double-click), or serve it:
```bash
cd portfolio-site
python3 -m http.server 8080   # then visit http://localhost:8080
```

## Deploy to GitHub Pages
1. Create a new repo on GitHub — e.g. `portfolio` (or `dbfournier.github.io` for a root URL).
2. From this folder:
   ```bash
   git remote add origin https://github.com/<your-username>/portfolio.git
   git branch -M main
   git push -u origin main
   ```
3. On GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: `main` / `/ (root)` → Save.**
4. Your site goes live at `https://<your-username>.github.io/portfolio/` within a minute or two.
   - If you named the repo `<your-username>.github.io`, it serves at `https://<your-username>.github.io/`.

### Custom domain (optional)
Add a `CNAME` file containing your domain (e.g. `donfournier.dev`), then point a DNS `CNAME` record at `<your-username>.github.io`. Enable HTTPS in Settings → Pages.

## Edit notes
- **Add LinkedIn / GitHub:** open `index.html`, find `const LINKS = { linkedin: "", github: "" };` near the bottom, and paste your URLs. They'll auto-appear in the hero and contact section.
- **Update résumé:** replace `assets/Don_Fournier_Resume.pdf`.
- All case-study copy lives inline in `index.html` under the `Selected Work` section; the full write-ups are in the parent `../portfolio/` folder.

> Confidentiality: case studies are genericized (no employer/customer/vendor names in the body, no exact internal financials, no confidential architecture). Phone and street address are intentionally omitted from this public page.
