# DILA

Entity matching project using DBLP and Scholar datasets. The work is split across two Jupyter notebooks:
- `task_01/01_entity_matching_pipeline.ipynb`: data cleaning, blocking, and candidate scoring.
- `task_02/02_feature_vector_and_ML_model.ipynb`: feature construction and ML model training/evaluation.

## Run instructions

### 1) Set up a virtual environment
```bash
python -m venv .venv
source .venv/bin/activate
pip install --upgrade pip
```

### 2) Install dependencies
```bash
pip install -r requirements.txt
```

### 3) Run the notebooks (recommended order)
```bash
jupyter notebook
```
Open and run:
1. `task_01/01_entity_matching_pipeline.ipynb`  
   This reads the raw CSVs from `data/` and produces intermediate outputs in `task_01/`, including `final_before_modelling.csv`.
2. `task_02/02_feature_vector_and_ML_model.ipynb`  
   This reads `task_01/final_before_modelling.csv` and produces `task_02/predictions.csv` and `task_02/best_model.joblib`.

## Data
Raw input files live in `data/`:
- `data/DBLP1.csv`
- `data/Scholar.csv`
- `data/DBLP-Scholar_perfectMapping.csv`

## Outputs
Notebook generated files are stored next to each notebook:
- `task_01/` contains candidate files and `final_before_modelling.csv`.
- `task_02/` contains `predictions.csv`, `best_model.joblib`, and figures.
