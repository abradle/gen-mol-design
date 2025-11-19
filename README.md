# Simple Generative Models Workshop (logP-driven)

**Goal:** Learn how property-driven generation works by implementing a tiny molecule generator and
optimizing a simple property (RDKit Crippen logP). Then **swap in a provided surrogate model**
and compare how the search behaves.

> This pack was generated on 2025-10-06.

## What students will do
1. Install dependencies (RDKit, SELFIES, scikit-learn).
2. Run a baseline generator that **maximizes RDKit logP** with light complexity penalty.
3. Swap the scoring function to a **given surrogate model** (Random Forest) and re-run.
4. Compare results (distributions, best molecules, novelty) and submit a short report.

## Quick start
### Option A: conda (recommended for RDKit)
```bash
# create and activate env
conda create -n genlogp -c conda-forge python=3.10 rdkit selfies scikit-learn pandas numpy matplotlib tqdm -y
conda activate genlogp
pip install joblib
# launch
jupyter lab  # or jupyter notebook, then open notebooks/
```

### Option B: pip
```bash
python -m venv .venv
source .venv/bin/activate  # (Windows): .venv\Scripts\activate
pip install --upgrade pip
pip install -r requirements.txt
jupyter lab  # or jupyter notebook
```

If `rdkit-pypi` fails on your platform, use **conda-forge** (Option A).

## Order of notebooks
1. `notebooks/01_setup_and_smoketest.ipynb`
2. `notebooks/02_baseline_logP_generator.ipynb`
3. `notebooks/03_tweak_with_surrogate_model.ipynb`

## Deliverables (students)
- `outputs/baseline_top50.csv` and `outputs/tweaked_top50.csv`
- 2–4 figures (logP distribution, objective trace, novelty vs. score, etc.)
- A short report (~2 pages) answering the questions outlined

## Safety / ethics
- This is a toy exercise optimizing **a single scalar**. It’s not a drug design pipeline.
- Do not interpret high logP as “better drug.” Discuss limitations and biases in your report.

