# shinnasa.github.io

Personal academic website of Shinpei Nakamura-Sakai — <https://shinnasa.github.io>

Built with Jekyll on GitHub Pages, using a trimmed-down fork of
[academicpages](https://github.com/academicpages/academicpages.github.io)
(itself a fork of [Minimal Mistakes](https://github.com/mmistakes/minimal-mistakes)).

## Structure

Four pages, all in `_pages/`:

| File | URL |
| --- | --- |
| `about.md` | `/` — bio, news, press |
| `publications.md` | `/publications/` |
| `teaching.md` | `/teaching/` |
| `cv.md` | `/cv/` |

Publications are hand-authored markdown in a single file rather than a Jekyll collection: the
entries carry multiple links, multiple venues, and nested award bullets, which the theme's
collection template cannot render. To add a paper, paste a new block into `_pages/publications.md`.

Navigation lives in `_data/navigation.yml`. PDFs live in `files/`.

## Local preview

```bash
bundle install
bundle exec jekyll serve --config _config.yml,_config.dev.yml
```

The second `--config` merges over the first (it does not replace it), setting
`url: http://localhost:4000` and unminified CSS. Google Analytics is suppressed outside of
production by the environment guard in `_includes/analytics.html`.

Then open <http://localhost:4000>.
