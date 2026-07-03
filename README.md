# IUAT static website draft

This is a draft physician-facing website for the International Unruptured Aneurysm Trial, built using the same single-master-markdown workflow as the supplied static site generator.

## What is included

- `index.html`: homepage
- generated internal pages for overview, rationale, design, outcomes, sites, eligibility, leadership, resources and register interest
- `master/iuat.md`: source content for generated pages
- `templates/standard.html`: page template
- `templates/index_pre.html`: homepage template
- `templates/footer.html`: shared footer fragment
- `css/main.css`: trial-specific styling
- `js/menu.js`: small helper script
- `img/`: IUAT logo and favicons
- `downloads/`: draft protocol and presentation files
- `build.py`: generator script adapted from the supplied static site generator

## Build command

From this folder run:

```bash
python3 build.py
```

Pandoc is required. I removed the dependency on `pandoc-crossref` to make the build easier to run on a standard setup.

## Before publishing

Replace the draft email address in `master/iuat.md`:

```text
iuat.trial@example.org
```

Then rebuild the site.

Also update the base URL in `build.py` or set it at build time:

```bash
SITE_BASE_URL="https://your-domain.example/" python3 build.py
```

## Notes

The site is written as a professional site-interest and credibility website. It deliberately avoids patient-recruitment language because IUAT is still in planning and is not yet open to patient enrolment.
