# pace-catalog-feed

Public, machine-readable course-availability data for [professional.ucsb.edu](https://professional.ucsb.edu),
generated hourly from UCSB PaCE's Zoho CRM by the workflow in the private repo
`UCSB-PaCE/pace-web` (`scripts/course_matrix/`). This repo holds generated files only.

Served by GitHub Pages from the `gh-pages` branch:

| URL | What |
|---|---|
| `https://ucsb-pace.github.io/pace-catalog-feed/course-matrix/` | human preview of every program page's matrix |
| `.../course-matrix/all.csv` | the course matrix rows (`Units, Fall, Winter, Spring, Summer, URL, Title, Course, Program`), the drop-in for the Drupal Feeds importer |
| `.../course-matrix/index.json`, `.../course-matrix/pages/<slug>.json` | per-page JSON: blocks, courses, quarter cells with state and section detail |
| `.../course-matrix/catalog/{courses,sections,programs,terms}.json` | the small catalog API |
| `.../course-matrix/reports/run.json`, `.../course-matrix/reports/stream-drift.md` | run summary and drift vs CRM certificate streams |

Columns always run Fall, Winter, Spring, Summer; a quarter that has finished rolls to the
next year's instance (the window is stamped in every file). `N/A` means no public,
final-approved section exists in the CRM for that quarter.

Questions: UCSB-PaCE/pace-web issue #5.
