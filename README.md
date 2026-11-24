# Project 2 — Cautious Growth Portfolio

Built with AI help for coding, research organization, debugging, and documentation; the analysis and committee decision are mine. Education, not investment advice.

This is the clean final-deliverables repository for FIN 439 Project 2. It contains only the runnable application and final-project evidence; earlier labs, prototypes, skills, reports, and recording scripts are intentionally excluded.

## Committee decision

The recommendation is a **monitored pilot**, not immediate full adoption. The pilot range is 55–65% BIL and 35–45% ACWI. The committee reviews or pauses the process if the latest-36-month stress moves an allocation by 25 percentage points or more compared with the all-history base window, if the portfolio misses the net-return target, or if the credit monitor flags LQD.

## Run the app

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
streamlit run app.py
```

The default app reads `prices.csv`, which contains monthly adjusted-close prices for BIL, IEF, LQD, and ACWI.

## Project structure

- `app.py` — Streamlit dashboard.
- `portfolio.py` — portfolio math, mandate checks, and allocation search.
- `prices.csv` — ETF price input.
- `docs/` — decision memo, validation and AI-use record, cold-run evidence, Lab 20 record, and submission manifest.
- `outputs/` — readable executed-output artifact.
- `videos/` — YouTube links and completed caption pages.
- `transcripts/` — completed corrected transcripts only; recording drafts are excluded.

## Current video evidence

- [Video 1](videos/video-1.md)
- Video 2: corrected captions are included; add the final YouTube link when available.
- [Video 3](videos/video-3.md)

## Limitations

- Historical return and volatility estimates are not forecasts.
- The allocation search uses five-percentage-point steps and can miss a better allocation between grid points.
- The credit-spread signal is a monitoring input, not an automatic trade rule.

See [the validation record](docs/validation-and-ai-use.md) and [submission manifest](docs/submission-manifest.md) for sources, tests, and submission status.
