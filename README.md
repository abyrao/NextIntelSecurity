# Mythos Intel Feed

An intelligence-style dark-theme dashboard for tracking AI model news and signals.
Built as a single self-contained HTML file — no build step, no dependencies.

## Live demo

Once deployed: `https://<your-username>.github.io/mythos-intel-feed`

## Features

- Dark terminal aesthetic with scanline header texture
- 6 signal categories: Release, Case Studies, Implementation, Lessons Learned, Remediation, Engineering
- Masonry card grid with staggered animations
- Filter by category, sentiment, and relevance score
- Sparkline trend charts per category
- Click any card to expand full analysis
- Skeleton loading state on refresh
- Optional live Anthropic API web search (enter your API key in the dashboard)

## Launch on GitHub Pages

### 1. Create the repo on GitHub

Go to https://github.com/new and create a repo called `mythos-intel-feed`.
Leave it empty (no README, no .gitignore).

### 2. Push from your local machine

Open a terminal in the folder containing `index.html` and run:

```bash
git init
git add index.html README.md
git commit -m "Initial commit: Mythos Intel Feed"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/mythos-intel-feed.git
git push -u origin main
```

Replace `YOUR_USERNAME` with your GitHub username.

### 3. Enable GitHub Pages

1. Go to your repo on GitHub
2. Click **Settings** → **Pages** (left sidebar)
3. Under **Source**, select **Deploy from a branch**
4. Set branch to `main`, folder to `/ (root)`
5. Click **Save**

Your site will be live at `https://YOUR_USERNAME.github.io/mythos-intel-feed` within ~60 seconds.

## Live search (optional)

Click **API KEY** in the dashboard header and enter an Anthropic API key to enable live web search.
The search uses the `web_search` tool to find recent news about Claude models and formats results
into the same card layout as the mock data.

> **Note:** Direct browser API calls may be blocked by CORS in some environments.
> If you see a CORS error, run the app through a local server (`python -m http.server 8080`)
> or add a lightweight proxy.

## Customise

All data, categories, and colours are defined at the top of the `<script>` block in `index.html`.
Edit `MOCK` to change demo articles, `CATS` to add/rename categories, and the CSS variables
at the top of `<style>` to retheme.
