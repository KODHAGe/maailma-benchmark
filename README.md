# maailma — benchmark site

Static GitHub-Pages site for the maailma news-source benchmark.

- **index.html** — landing page linking the two views
- **benchmark.html** — country-by-country benchmark table (top-3 vs Reuters DNR reference, full metrics, filters, clickable links)
- **analysis_report.html** — cross-market analysis report with improvement actions

## Regenerate

From the maailma project root:

```sh
.venv/bin/python -m tests.benchmark_analysis
.venv/bin/python -m tests.render_benchmark
.venv/bin/python -m scripts.analysis_report
cp benchmark.html analysis_report.html site/
```

Then commit and push from this folder (`site/` is its own git repo).
