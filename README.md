# Academic Homepage

This repository is a bilingual academic personal homepage based on
[multi-language-al-folio](https://github.com/george-gca/multi-language-al-folio),
a multilingual fork of [al-folio](https://github.com/alshedivat/al-folio).

The current site is configured for English and Chinese:

- English root: `/`
- Chinese root: `/zh/`
- GitHub Pages target: `https://liang-hongtao.github.io`

## Replace Personal Information

Edit these files first:

- `_config.yml` - name, URL, keywords, global site settings.
- `_pages/en-us/about.md` and `_pages/zh/about.md` - homepage biography.
- `_data/socials.yml` - email, GitHub, Google Scholar, ORCID, ResearchGate.
- `_bibliography/papers.bib` - publications.
- `_projects/en-us/` and `_projects/zh/` - project cards and pages.
- `_news/en-us/` and `_news/zh/` - dated news items.
- `_data/en-us/cv.yml` and `_data/zh/cv.yml` - CV content.
- `assets/img/profile-placeholder.svg` - replace with a real portrait.

## Local Preview

Install Ruby and Bundler if needed, then run:

```bash
bundle install
bundle exec jekyll serve
```

Open:

```text
http://127.0.0.1:4000
```

## Publish on GitHub Pages

Create a GitHub repository named exactly:

```text
liang-hongtao.github.io
```

Then push this folder:

```bash
cd academic-homepage
git add .
git commit -m "Create academic homepage"
git remote add origin https://github.com/liang-hongtao/liang-hongtao.github.io.git
git push -u origin main
```

In GitHub repository settings, set **Pages** to deploy from **GitHub Actions**.
The workflow in `.github/workflows/deploy.yml` builds the Jekyll site and deploys
the generated `_site` output.

## Attribution

The site foundation comes from `multi-language-al-folio`, which is MIT licensed.
Keep `LICENSE` in this repository and do not reuse other researchers' personal
content, publications, analytics scripts, or registration information.
