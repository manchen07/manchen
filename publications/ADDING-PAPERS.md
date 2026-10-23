# Add or update a publication

1. Copy `_paper-template.yml` into `papers/` and rename the copy (for example, `my-new-paper.yml`).
2. Fill in the title, date (`YYYY-MM-DD`), authors in their original order, and journal citation. Set `work-type: methodological` for methods development, evaluation, and tutorials, or `work-type: applied` for studies answering substantive research questions. Use these exact lowercase values so the paper appears in the intended section. Keep text in quotes. Escape an embedded double quote with a backslash, or use single quotes around the whole value.
3. Replace the resource URLs. Delete any link you do not have; never leave `REPLACE-ME` in a published entry. You can add more links by repeating a `text`/`href` pair.
4. Optionally add `abstract` for a collapsible abstract. Only add text you are permitted to republish.
5. Save, then run `quarto render publications/index.qmd` or preview that page in RStudio. The page automatically discovers `papers/*.yml`, places each paper in its section, orders entries newest first within each section, and updates each section's filter.
6. Commit the edited source files and rendered `docs/` output, then push to GitHub.

Use one YAML file per paper. Each file starts with `- title:` (it contains a one-item list). Keep the indentation shown in the template. Remove a paper by moving its YAML file outside `papers/` and rendering again. The layout is in `_publications.ejs.md`; you do not need to edit it for new papers.

The filter searches title, authors, journal, and displayed year. Your name is emphasized automatically when written exactly as `Man Chen`. Resource buttons are keyboard-accessible links, and entries stack on small screens.

## Initial sources and scope

The initial nine records are the entries listing Man Chen as a coauthor on https://jepusto.com/publications/, retrieved October 23, 2026. Citation details, author order, dates, and resource destinations were transcribed from that listing; abstracts, full papers, and layout code were not copied. This is the overlap with that page, not a claim to include your complete publication history. Resource links were copied from the source but their contents were not individually audited.

Dates follow the source listing (which can reflect online publication rather than the final issue date). Check the final journal citation and date when updating a paper. Each YAML file retains a source comment. The listing layout and CSS were written for this site.

Six additional peer-reviewed journal articles without James Pustejovsky as a coauthor were added from `files/Chen-CV-Github.pdf`, pages 1–3. Their author order, citation years, journal details, and DOI links follow the CV. Coauthor initials are retained rather than guessing full names; Man Chen is expanded for consistent highlighting. These entries use January 1 as an internal sorting placeholder because the CV gives only a year; the website displays only the year. Ordering within those years is approximate. No submissions, non-peer-reviewed articles, or conference presentations were included.
