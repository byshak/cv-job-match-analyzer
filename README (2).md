# Shortlist: Free CV & Job Description Match Analyzer

Paste your CV and a job description. Get a transparent match score, the keywords you are missing, and bullet templates, all in your browser. **No backend, no API keys, no sign-up, no data leaves your device.**

[![License: MIT](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
![Dependencies](https://img.shields.io/badge/dependencies-0%20(pdf.js%20on%20demand)-brightgreen)
![Privacy](https://img.shields.io/badge/privacy-100%25%20local-blue)

**Live demo:** https://byshak.github.io/cv-job-match-analyzer/

## Features

- Overall CV-to-job match score (0-100) with an animated dashboard
- Missing and matched keywords, with recognised skills highlighted
- Import a CV or job ad from PDF, DOCX or TXT. Files are read in your browser and never uploaded (PDF reading loads pdf.js from cdnjs on demand)
- 200+ recognised skills and synonym handling (JS = JavaScript, K8s = Kubernetes, Postgres = PostgreSQL)
- Specific suggestions and copyable bullet-point templates
- Deterministic scoring: the same input always gives the same score
- One self-contained `index.html`: plain HTML, CSS and vanilla JavaScript
- Responsive, keyboard-accessible, respects reduced-motion settings

## How the score is calculated

| Component | Weight | Measured by |
|---|---|---|
| Keyword / skill coverage | 50% | Top 30 job keywords; recognised skills count 2x |
| Important phrases | 20% | Two-word phrases repeated in the job description |
| Job-title alignment | 15% | Detected title versus the CV |
| Experience signals | 15% | Years, degree, certification, measurable results, action verbs |

If a component cannot be measured, its weight is shared among the others. Matching ignores case and treats simple plurals as equal.

## Pages

`index.html` (analyzer), `guides.html` plus four guides, `match-intelligence.html`, `how-scoring.html`, `404.html`. Each page is self-contained (CSS and JS are inlined).

## Run it

Download `index.html` and open it in a browser. Or host it free with GitHub Pages: **Settings > Pages > Deploy from branch > main / root**.

## Privacy

Everything runs locally in your browser. Nothing is uploaded, tracked or stored.

## Disclaimer

Results are guidance only. This tool does not simulate any real applicant tracking system and cannot guarantee ATS approval, interviews or job offers.

## Roadmap

- [x] File import: PDF, DOCX, TXT (read locally)
- [ ] OCR for scanned PDFs
- [ ] Larger skills dictionary and more languages
- [ ] Export report as PDF

Ideas and pull requests are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md).

## Keywords

CV analyzer, resume analyzer, ATS keyword checker, resume keyword scanner, job description match, CV job match, resume optimizer, vanilla JavaScript, no-backend tool.

## License

[MIT](LICENSE)
