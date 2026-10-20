# DSCI 552 Homework 4

Name: Shanglin Jiang

GitHub username: sjiang83-corgi

## Files

- `notebook/Jiang_Shanglin_HW4.ipynb`: solutions to Questions 2, 3, and 4, including saved outputs.
- `data/AReM/`: unchanged source recordings and documentation.
- `results/`: CV search tables, model comparisons, coefficients, and figures.
- `requirements.txt`: dependencies; scientific package versions match the tested Python 3.10 environment.

## Run

Use Python 3.10. Install requirements and run the notebook from its own folder, or execute from the repository root:

```bash
python -m pip install -r requirements.txt
python -m nbconvert --to notebook --execute --inplace notebook/Jiang_Shanglin_HW4.ipynb --ExecutePreprocessor.timeout=7200
```

All data paths are relative. The full searches can take several minutes or longer depending on hardware. Raw recordings are segmented locally; scaling and RFE are fitted inside each CV training fold. Both tasks use five stratified folds. In multiclass CV, one validation fold lacks bending2 because there are only four such training recordings; accuracy is still valid, every training fold includes all classes, and AUC is evaluated on the test set containing all classes. All 20 segment counts are evaluated. The notebook declares the feature-count and regularization grids and reports numerical diagnostics.

## Submission

Publish these folders and files directly at the root of the homework repository. Keep all notebook outputs. The original assignment PDF is retained locally and ignored by Git. This preparation does not create or publish a GitHub repository.
