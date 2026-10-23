# Updating teaching

Edit `teaching/index.qmd` to update descriptions and terms taught. Each course has one section and a collection of syllabus links, newest first.

To add a new offering:

1. Copy its PDF to `files/syllabi/` with a descriptive name, such as `hlm-fall-2027.pdf`.
2. Add the term to the course's terms taught.
3. Copy an existing syllabus button and update its term and relative PDF path.
4. Run `quarto render teaching/index.qmd` and check the link in Preview.
5. Commit the source, PDF, and rendered `docs/` files when ready to publish.

The initial six PDFs are unchanged copies of the supplied syllabi. Descriptions, course numbers, credits, prerequisites, and terms were taken from their opening pages. Only syllabus downloads are included; lecture materials, assignments, and course assessments have not been added.
