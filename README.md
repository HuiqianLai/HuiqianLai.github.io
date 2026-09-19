# huiqianlai.github.io

Personal homepage of Huiqian (Mia) Lai, built with Jekyll and the
[Minimal Light](https://github.com/yaoyao-liu/minimal-light) theme.

## Editing

| What                         | Where                                        |
| ---------------------------- | -------------------------------------------- |
| Name, title, links, avatar   | `_config.yml`                                |
| About, news, teaching, media | `index.md`                                   |
| Publications & talks         | `_data/publications.yml`                     |
| Layout / styling             | `_layouts/homepage.html`, `assets/css/custom.css` |

## Local preview

```bash
bundle install
bundle exec jekyll serve   # http://localhost:4000
```

## Deployment

Pushes to `main` trigger `.github/workflows/jekyll.yml`, which builds the site and
publishes it to GitHub Pages (Settings → Pages → Source must be "GitHub Actions").
