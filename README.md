# Enriching Early Learning — Jekyll Site Setup

This folder is a complete, ready-to-deploy Jekyll site: 40 blog posts, 39 pages,
75 images, your theme, and all 1,565 historical comments preserved and displayed
per-post. Follow these steps in order.

## STEP 1 — Create the GitHub repository

1. Go to https://github.com and sign in (or create a free account if you don't have one).
2. Click the "+" icon top-right → "New repository".
3. Name it anything — e.g. `enriching-early-learning-site`. It does NOT need to
   match your domain name.
4. Set it to **Public** (required for free GitHub Pages + free giscus comments).
5. Do NOT initialize with a README, .gitignore, or license — leave it empty.
6. Click "Create repository".

## STEP 2 — Upload this site into the repo

Easiest method if you're not comfortable with git/command line:

1. Install **GitHub Desktop** (free): https://desktop.github.com
2. Open it, sign in with your GitHub account.
3. File → Add Local Repository → select this unzipped folder.
4. It will say "this folder is not a git repository, create one?" — say yes.
5. Click "Publish repository" and pick the repository you created in Step 1.
6. Done — all files upload automatically.

Alternative (if you're comfortable with Terminal):
```
cd path/to/this/unzipped/folder
git init
git add .
git commit -m "Initial site migration"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
git push -u origin main
```

## STEP 3 — Enable GitHub Pages

1. In your repo on GitHub.com, go to **Settings** → **Pages** (left sidebar).
2. Under "Build and deployment", Source: select **Deploy from a branch**.
3. Branch: select **main**, folder **/ (root)** → Save.
4. Wait 1-2 minutes. Refresh the page — you'll see a green box with your live
   test URL, something like: `https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/`
5. **Test this URL thoroughly** — click through posts, pages, images, before
   touching your real domain. Bluehost stays completely untouched during this step.

## STEP 4 — Point your custom domain (only after Step 3 is confirmed working)

1. Still in Settings → Pages, scroll to "Custom domain".
2. Enter `www.enrichingearlylearning.com` and Save.
   (This matches the CNAME file already included in this repo.)
3. In GoDaddy, go to your domain's DNS management and add these records:
   - Type: CNAME, Name: www, Value: YOUR-USERNAME.github.io
   - Type: A, Name: @, Value: 185.199.108.153
   - Type: A, Name: @, Value: 185.199.109.153
   - Type: A, Name: @, Value: 185.199.110.153
   - Type: A, Name: @, Value: 185.199.111.153
4. DNS changes can take up to 24-48 hours to fully propagate, though often
   much faster. Your Bluehost site keeps working the entire time until DNS
   actually switches over — there's no downtime window where nothing works.
5. Back in GitHub Pages settings, once DNS is detected, check "Enforce HTTPS".

## STEP 5 — Set up giscus for new comments

Your OLD comments (1,565 of them) are already built into every post as a
static historical record — no setup needed, they just work.

For NEW comments going forward:

1. Go to https://github.com/apps/giscus and install it on your new repository.
2. In your repo → Settings → General → scroll to "Features" → enable **Discussions**.
3. Go to https://giscus.app
4. Enter your repo name (`YOUR-USERNAME/YOUR-REPO-NAME`) in the setup form.
5. It will generate 4 values: `data-repo-id`, `data-category`, and `data-category-id`.
6. Open `_config.yml` in this repo and fill them in:
   ```
   giscus:
     repo: "YOUR-USERNAME/YOUR-REPO-NAME"
     repo_id: "PASTE-HERE"
     category: "Comments"
     category_id: "PASTE-HERE"
   ```
7. Commit that change — new comments will now work on every post automatically.

## What's already done for you in this repo

- `_posts/` — all 40 blog posts, exact original URLs preserved via `permalink:`
- `*.md` files at root — all 39 pages
- `assets/images/` — all 75 images, wired into matched posts
- `_data/comments.json` — all 1,565 historical comments, auto-rendered per-post
- `assets/css/main.css` — full theme (ADLaM Display, Inter, your brand colors)
- `index.html` — homepage matching your original design
- `CNAME` — pre-filled with your domain

## Known open items (not blockers, but worth finishing)

- 20 of 40 posts don't have a confirmed image match yet — see the "pending image"
  list from earlier in our conversation.
- HubSpot form on the Professional Development Hub page now uses Formspree —
  needs a real Formspree form ID swapped in (currently a placeholder).
- Some deeper program pages (Little Social Stars Curriculum, coaching pages)
  may need further layout polish once you see them live.
