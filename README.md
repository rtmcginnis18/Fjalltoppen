# Fjalltoppen

Personal site — research, art & projects, and blog. Built with [Hugo](https://gohugo.io),
deployed to GitHub Pages via GitHub Actions, served at https://fjalltoppen.com.

## Local development

```bash
hugo server -D
```

Visit http://localhost:1313. `-D` includes draft content.

## Adding content

```bash
hugo new content posts/my-post.md       # blog post
hugo new content research/my-topic.md   # research entry
hugo new content projects/my-project.md # art/project entry
```

Add `tags: ["tag-one", "tag-two"]` to any post's front matter to tag it —
tag pages are generated automatically at `/tags/`.

## Deploying

Push to `main` — `.github/workflows/hugo.yml` builds and deploys to GitHub
Pages automatically. No manual build step needed.

## Turning on optional features

Edit `hugo.toml` under `[params]`:

- **Visit counter** — sign up at [GoatCounter](https://www.goatcounter.com/),
  set `goatCounterCode` to your site code (the part before `.goatcounter.com`).
- **Comments** — enable GitHub Discussions on this repo, configure
  [giscus.app](https://giscus.app) for `rtmcginnis18/Fjalltoppen`, and copy the
  four generated values into `giscusRepo`, `giscusRepoId`, `giscusCategory`,
  and `giscusCategoryId`.

## Structure

- `content/` — Markdown content (posts, research, projects, about)
- `layouts/` — HTML templates (base, header/footer partials, list/single views)
- `static/` — CSS, favicons, OG image (copied to site root as-is)
- `.github/workflows/hugo.yml` — build + deploy pipeline
