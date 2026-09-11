# Setup — publishing this as your jxjwilliam profile README

GitHub renders a profile README when a repo's **name matches your username exactly**
and is **public**. For this account that repo is `jxjwilliam/jxjwilliam`.

## 1. Create the repo
On GitHub, create a new **public** repository named exactly `jxjwilliam` under the
`jxjwilliam` account. Do not initialize it with a README (you already have one here).

## 2. Push this scaffold
```bash
cd jxjwilliam
git init
git remote add origin https://github.com/jxjwilliam/jxjwilliam.git
git add .
git commit -m "Initial profile README"
git branch -M main
git push -u origin main
```

## 3. Enable workflow write permissions
Both workflows commit back to the repo, so they need write access:
- Go to **Settings → Actions → General → Workflow permissions**
- Select **"Read and write permissions"**
- Save

## 4. Trigger the workflows once
- Go to **Actions** tab → select **"Generate contribution snake"** → **Run workflow**
- Same for **"Update recent activity in README"**

These also run on a schedule afterward (snake: daily, activity: every 6 hours), so the
profile keeps itself current with zero further maintenance.

## 5. Verify
Visit `https://github.com/jxjwilliam` — the README, tech stack, lab log, live stats
cards, activity feed, and contribution snake should all render.

## Notes / things to check before publishing
- The stats widgets (`github-readme-stats.vercel.app`) are a shared public instance —
  if it's ever rate-limited or down, the images just won't load; nothing breaks.
- The "Lab Log" table links to four real repos already on your account
  (`jinyong-finetune-qlora`, `wuxia-jiangyunxing`, `github-radar`, `ms-apollo-graphql`).
  Swap these out any time a newer experiment is more representative.
- `hero-banner.svg` uses only system monospace fonts and a CSS `<animate>` blink on the
  cursor — GitHub's Camo proxy renders both fine.
