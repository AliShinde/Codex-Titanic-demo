# Titanic pandas workshop

`analysis.py` introduces missing-value checks, pandas grouping, and descriptive
survival rates. Comments explain the calculations. It uses `train.csv` for observed
survival outcomes and checks missing values in both training and test data.
`gender_submission.csv` is a sample submission, not observed outcomes.

[titanic_analysis.ipynb](titanic_analysis.ipynb) contains the analysis code and
executed results, with both charts displayed inline. Run its cells from top to
bottom with the repository as the notebook working directory. The calculations
match `analysis.py`; only the data-directory setup differs for a notebook.

With Python 3.12, install `requirements.txt` in a virtual environment and run:

```bash
python -m pip install -r requirements.txt
python analysis.py
```

To rerun the notebook interactively in the same virtual environment:

```bash
python -m pip install -r requirements.txt jupyterlab==4.6.4
jupyter lab titanic_analysis.ipynb
```

In the prepared cloud environment:

```bash
source /workspace/.setup/titanic/env.sh
python /workspace/Codex-Titanic-demo/analysis.py
```

The script saves missing-value counts, survival tables by `Pclass`, `Sex`, and their
joint groups, two labeled PNG charts, and [a short summary](outputs/summary.md) in
`outputs/`. Use `--output-dir /path/to/output` to choose another destination.
It validates IDs, binary outcomes, and group totals before reporting results.
It does not fill missing data, train models, or infer causation.
