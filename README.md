# bols-survey

Faculty Delphi survey for OB/GYN board exam topic prioritization.

**Live page**: https://vicentidoc.github.io/bols-survey/

## Visibility — intentionally PUBLIC for GitHub Pages

This repository is deliberately public so GitHub Pages can serve the survey to faculty respondents. The contents are safe to be public **by design**:

- **No PHI** — no patient records, lab values, or clinical identifiers
- **No personally identifying faculty data** — responses POST to a Google Apps Script Web App and are stored in a private Google Sheet, not in this repo
- **HTML payload is structural only** — Delphi questionnaire wording + form scaffold; no embedded data
- Subject-matter Chinese phrases (e.g., "高危險產[婦]") may match generic name regexes as false positives; they refer to clinical topics, not individuals

Audit: 2026-04-29 (confirmed safe; user-validated intent: keep public).

## Structure

- `index.html` — single-page survey form (Vue.js inline)
- Form action: Google Apps Script Web App URL (URL-as-key auth model)
- Backing store: private Google Sheet owned by maintainer

## Maintenance

Edit `index.html` directly; commit; GitHub Pages redeploys automatically. New surveys should follow the survey-toolkit SOP (`E:/Vicent_E/AI_Evolution/templates/survey-toolkit/`) and use a `/{survey-id}/` subdirectory rather than the legacy root path.
