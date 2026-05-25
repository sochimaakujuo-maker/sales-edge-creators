# Sales Edge Creators — Update Instructions

The site is already live on Vercel. Every time you edit a page, run these commands.

---

## Step 1 — Copy updated files from DWCP to SEC-Deploy

```bash
cd "C:\Users\sochi\OneDrive\SEC-Deploy"

copy "..\DWCP\SEC-LinkedIn-Sales-Activation.html" .
copy "..\DWCP\SEC-Book-A-Call.html" .
copy "..\DWCP\SEC-Revenue-Accelerator-Landing.html" .
copy "..\DWCP\SEC-Pipeline-Sprint-Landing.html" .
```

Only copy the files you actually changed. Copying all four is always safe.

---

## Step 2 — Commit and deploy

```bash
git add . && git commit -m "Update pages" && git push origin main
vercel --prod
```

That's it. Vercel reads `.vercel/project.json` and deploys to the correct project automatically.

---

## Key details (do not change without updating all pages)

| | |
|---|---|
| Vercel project | `sales-edge-creators` |
| Team slug | `sochimaakujuo-1785s-projects` |
| Canada phone | 1-647-474-1661 |
| US phone | 1-526-365-7222 |
| Calendly | https://calendly.com/oneaway/eclub |
| LinkedIn | https://www.linkedin.com/in/lincoln-anthony-hol/ |

---

## Page routing reference

| URL | File |
|-----|------|
| `/` | SEC-LinkedIn-Sales-Activation.html |
| `/sales-activation` | SEC-LinkedIn-Sales-Activation.html |
| `/book` | SEC-Book-A-Call.html |
| `/sales-edge-book` | SEC-Book-A-Call.html |
| `/revenue-accelerator` | SEC-Revenue-Accelerator-Landing.html |
| `/activation-sprint` | SEC-Pipeline-Sprint-Landing.html |
