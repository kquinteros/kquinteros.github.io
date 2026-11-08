# Blog workflow

Goal: at least one post a month. Quarto ignores this `_blog/` folder (names starting with `_` are skipped), so nothing here gets rendered or listed.

## Monthly cadence: publish on the last Sunday

| When | Do |
|---|---|
| 1st weekend | Choose a topic from the backlog below. Copy the template and leave `draft: true`. Write a 5-bullet outline. |
| 2nd–3rd weekend | Write the body, then add figures, code and references. |
| 3rd weekend | Finish the draft. Read it once in `quarto preview`, where drafts still show. |
| **Last Sunday** | Run the publish checklist below. |

If a month gets away from you, publish a short post (a protocol tweak, a figure with a paragraph, a reading note). A short post still counts.

Publish days for the next year: 2026-11-29, 2026-12-27, 2027-01-31, 2027-02-28, 2027-03-28, 2027-04-25, 2027-05-30, 2027-06-27, 2027-07-25, 2027-08-29, 2027-09-26, 2027-10-31.

## New post

```bash
mkdir posts/2026-11-29-short-slug
cp _blog/post-template.qmd posts/2026-11-29-short-slug/index.qmd
```

- Name the folder `YYYY-MM-DD-lowercase-slug`. Name the file `index.qmd`, which gives the URL `/posts/<folder>/` and avoids the `-p1`/`-p2` problem when two posts share a date.
- Keep data, figures and PDFs inside the post's folder. Shared stock images go in `images/`.

## Publish checklist

- [ ] `date:` is today's date and matches the folder name
- [ ] `description` is 1–2 sentences, and `image` points to a file that exists
- [ ] `categories` come from the list below (add `R` if the post has R code, since the RSS feed only includes `R`)
- [ ] Headings use `##`/`###` with no `**bold**` inside, and no stray `#` headings
- [ ] Figures have alt text, and links work
- [ ] `draft: false`
- [ ] `quarto render` runs locally (posts are `freeze: true`, so commit the updated `_freeze/`)
- [ ] Commit, push, then run `quarto publish gh-pages`

## Categories in use

Biodiversity, DNA, Ficus, Genomics, Method, Misc., Molecular Biology, NGS, R, Spatial Analysis

## Topic backlog

- [ ] Finish the **historical DNA** draft (`posts/2025-10-29-Hist-DNA/`). It's nearly ready to post.
- [ ] B.E.S.T. libraries follow-up: what changed with more samples
- [ ] DLO Hi-C: first results or troubleshooting notes
- [ ] Fig wasp communities: a short explainer for non-specialists
- [ ] Update to the *Ficus* occurrence maps with new collections
