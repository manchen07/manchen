# Updating software

Edit `software/index.qmd`. Each project has one heading, a short description, coauthor credits, and resource buttons. Keep package and associated app links together. The right-side project navigation is generated from the headings.

The initial scope is the five software entries on page 4 of `files/Chen-CV-Github.pdf`: three R packages and two associated web applications. Descriptions and destinations were checked against these project documentation pages:

- https://jepusto.github.io/lmeInfo/
- https://jepusto.github.io/scdhlm/
- https://jepusto.github.io/SingleCaseES/

James's overview at https://jepusto.com/software/ was also consulted. scdhlm's overview credits use Bethany H. Bhat, while the CV and documentation's versioned citations use Hamilton; this page retains the CV citation form instead of silently changing that attribution. SingleCaseES credits follow the CV and documentation's citation order. No current version numbers are claimed.

To update, check the project's citation guidance and documentation, edit the entry, then run `quarto render software/index.qmd`. Commit source and generated `docs/` changes when ready to publish.
