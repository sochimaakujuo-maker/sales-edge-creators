# Sales Edge Creators — Deploy Instructions for Claude Code

## What This Is
Three static HTML pages for Sales Edge Creators, deployed as a Vercel static site.

| Page | File | Live URL |
|------|------|----------|
| Revenue Accelerator | SEC-Revenue-Accelerator-Landing.html | yourdomain.vercel.app/ |
| Pipeline Sprint     | SEC-Pipeline-Sprint-Landing.html     | yourdomain.vercel.app/sprint |
| Book a Call         | SEC-Book-A-Call.html                 | yourdomain.vercel.app/book |

Vercel project name: **sales-edge-creators**
Vercel team: **sochimaakujuo-1785s-projects**
GitHub account: **sochimaakujuo@gmail.com**

---

## First-Time Setup (run once)

Run these commands from inside this folder (`SEC-Deploy/`):

```bash
# 1. Initialise git repo
git init
git add .
git commit -m "Initial commit — Sales Edge Creators"

# 2. Create GitHub repo and push
#    (requires GitHub CLI — run `gh auth login` first if needed)
gh repo create sales-edge-creators --public --source=. --remote=origin --push

# 3. Deploy to Vercel
#    (requires Vercel CLI — run `npm i -g vercel` if not installed)
vercel --prod --yes --name sales-edge-creators --team sochimaakujuo-1785s-projects
```

After first deploy, Vercel will create a `.vercel/project.json` — commit that so future deploys are automatic.

---

## Updating the Pages (after edits)

Whenever the HTML files are updated, run:

```bash
git add .
git commit -m "Update SEC pages"
git push origin main
vercel --prod
```

Or if Vercel is connected to GitHub via the dashboard, pushing to GitHub will auto-deploy.

---

## File Structure
```
SEC-Deploy/
├── SEC-Revenue-Accelerator-Landing.html   ← main offer page (serves at /)
├── SEC-Pipeline-Sprint-Landing.html       ← sprint page (serves at /sprint)
├── SEC-Book-A-Call.html                   ← booking page (serves at /book)
├── vercel.json                            ← routing config
├── .gitignore
└── CLAUDE.md                              ← this file
```

## Important Notes
- All internal links between pages use relative filenames (e.g. `href="SEC-Book-A-Call.html"`). Vercel rewrites handle the clean URLs.
- The Stripe payment link is: https://buy.stripe.com/6oU5kEe4zfLJ0wzbIp2Fa0c
- The Calendly link is: https://calendly.com/oneaway/eclub
- Lincoln's LinkedIn: https://www.linkedin.com/in/lincoln-anthony-hol/
- **TODO:** Update `https://www.linkedin.com/in/lincoln-anthony-hol/` across all pages with Lincoln's exact LinkedIn URL if different.
- **TODO:** Add a custom domain in Vercel dashboard once live (Settings → Domains).
