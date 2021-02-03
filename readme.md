## Project Structure

```bash
.
└── project_root/
    ├── src/
    │   ├── data/
    │   │   ├── get_data.py (top-level data fetching functions for DB, static files, master table etc)
    │   │   ├── components/
    │   │   │   ├── component_1.py
    │   │   │   ├── component_2.py
    │   │   │   ├── ...
    │   │   │   ├── pipeline_1.py
    │   │   │   ├── pipeline_2.py
    │   │   │   ├── ...
    │   │   │   ├── query_1.sql
    │   │   │   └── query_2.sql
    │   │   └── saved_data (for small datasets)/
    │   │       ├── raw/
    │   │       ├── interim/
    │   │       └── processed/
    │   ├── exploratory/
    │   │   ├── whiteboard.py
    │   │   ├── exploratory.py
    │   │   ├── exploratory.ipynb
    │   │   └── plots/
    │   │       ├── graph1.png
    │   │       └── ...
    │   ├── preprocessing/
    │   │   ├── preprocess_script_1.py
    │   │   └── preprocess_script_2.py
    │   ├── train/
    │   │   ├── readme.md (optional)
    │   │   ├── get_training_data.py (gets train-test data for ML)
    │   │   ├── train.py (should contain cross-validation, optimisation and mlflow functions)
    │   │   ├── train_run.py (that calls the training script and submit jobs to Azure or local machine)
    │   │   ├── plots/
    │   │   │   ├── graph1.png
    │   │   │   └── ...
    │   │   └── components/
    │   │       ├── training_component_1.py
    │   │       ├── training_component_2.py
    │   │       ├── ...
    │   │       ├── plotting_component_1.py
    │   │       └── ...
    │   ├── eval_test/
    │   │   ├── readme.md (optional)
    │   │   ├── get_holdout_data.py
    │   │   ├── eval.py
    │   │   └── eval_run.py
    │   └── notebooks/ (only to walk stakeholders through findings if needed)
    ├── models/
    │   ├── interim_models/
    │   │   └── components (e.g. scalers, preprocessors)/
    │   └── final_models/
    │       └── components (e.g. scalers, preprocessors)/
    ├── deployment/
    │   ├── readme.md (optional)
    │   ├── deploy.py (for Azure)
    │   ├── docker_entry.py (for Docker container)
    │   └── ...
    ├── tests/
    │   ├── test_1.py
    │   └── ...
    ├── docs/
    │   ├── references/ (contains data dictionary, source mapping etc)
    │   ├── notes/ (contains discussions and meeting minutes)
    │   ├── reports/ (contains pdf, words, html report etc)
    │   └── plots/ (contains publication quality images and charts for the reports)
    ├── environment.yml/requirements.txt
    ├── Dockerfile
    ├── config.yml/config.txt (no authentication params)
    ├── .gitignore
    ├── .dockerignore
    └── readme.md
```