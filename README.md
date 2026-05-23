# Trading Ark — Landing Page

## Deploy to Vercel (correct way)

The file structure MUST be flat at the repo root. Like this:

```
your-repo/
├── index.html          ← AT THE ROOT, not in a subfolder
├── assets/
│   ├── hero-desk.png
│   ├── logo-full.png
│   ├── logo-mark.png
│   ├── payout-1.png
│   ├── payout-2.png
│   └── payout-mff.png
└── README.md
```

### Steps

1. Create a new GitHub repo (empty, no README)
2. On your computer: unzip this download into a folder
3. Open terminal in that folder. Run:
   ```bash
   git init
   git add .
   git commit -m "ship it"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO.git
   git push -u origin main
   ```
4. Go to vercel.com → Add New Project → Import your repo
5. Framework Preset: **Other** (it's just static HTML)
6. Root Directory: **leave empty** (must be repo root)
7. Click Deploy

### Why images don't load (common causes)

- **`index.html` is in a subfolder** instead of repo root → move it to root
- **Mac uploaded files with wrong case** (e.g. `Assets/` instead of `assets/`) → rename to lowercase
- **You drag-dropped only the HTML** into Vercel and skipped the assets folder → drop the whole folder
- **`.gitignore` excluded images** → check `git status` to confirm assets are tracked

### Test locally first

Before deploying, run this in the folder to test:
```bash
python3 -m http.server 8000
```
Open http://localhost:8000 — if images don't load here, they won't load on Vercel either.
