# toufiq.github.io

Personal website of **Toufiq Hamid**, built with [Jekyll](https://jekyllrb.com/)
(minima theme) and deployed to GitHub Pages via GitHub Actions.

🌐 **Live site:** https://toufiq171.github.io

## Structure

| Path | Purpose |
|------|---------|
| `index.md` | Homepage |
| `projects.md` | Project showcase |
| `about.md` | About / contact |
| `_config.yml` | Jekyll site configuration |
| `notebooks/ai-video-agent.ipynb` | Colab notebook: AI script-to-video agent experiment |
| `.github/workflows/jekyll-gh-pages.yml` | Build & deploy workflow |

## Local development

```bash
gem install bundler jekyll
jekyll serve
# open http://localhost:4000
```

Pushes to `main` deploy automatically.
