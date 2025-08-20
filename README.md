# Students' Adaptability in Online Education

A data analytics project based on my diploma research studying factors that influence how students adapt to online learning.  
This repository organises the dataset, notebook, and a clear write-up so recruiters can review the work quickly.

## Project Overview
- **Goal:** Explore which factors (internet, device, institution type, LMS, age, etc.) are associated with students' adaptability to online education and build simple ML models to classify adaptability levels.
- **Dataset:** 1,205 observations with 14 variables (demographics, institution context, connectivity, device, class duration, LMS availability, etc.).
- **Target:** Adaptability level with 3 classes: *Low, Moderate, High* (encoded numerically for modeling).
- **Models:** Decision Tree and Support Vector Machine (linear SVM).

## Key Results (from my research)
- Decision Tree achieved **~91.2% accuracy**, with strong precision/recall for the *Moderate* class; SVM achieved **~74% accuracy** overall.  
- Feature-importance (LIME) indicated **Institution Type** and **Institution's LMS availability** as among the most influential predictors, alongside class duration, IT-student status, age, internet type, financial condition, education level, and network type.

> See the `report/` summary and the notebook in `notebooks/` for details.

## Repository structure
```
students-adaptability-online-education/
├── analysis/                      # optional scripts or exported results
├── data/                          # dataset (Excel/CSV)  [large files ignored by .gitignore to keep repo light]
├── images/                        # charts/screenshots
├── notebooks/
│   └── students_adaptability_analysis.ipynb
├── report/
│   └── summary.md                 # plain-English summary of methods and findings
├── .gitignore
├── requirements.txt
└── README.md
```

## How to run locally
1. Clone this repository and create a virtual environment:
   ```bash
   python -m venv .venv
   .venv\Scripts\activate        # on Windows
   # source .venv/bin/activate     # on Mac/Linux
   pip install -r requirements.txt
   ```
2. Open the notebook:
   ```bash
   jupyter notebook notebooks/students_adaptability_analysis.ipynb
   ```
3. (If you don't have the dataset yet) place the Excel/CSV file into `data/` and update the path in the notebook.

## Methods
- **Preprocessing:** label/ordinal encoding; basic cleaning; train/test split.
- **Models:** `DecisionTreeClassifier` and `LinearSVC` (one-vs-one), with performance evaluated via Accuracy, Precision, Recall and F1. ROC/AUC visualised for multi-class via one-vs-rest.
- **Explainability:** Example LIME explanations to inspect influential features for each class prediction.

## Visualizations

### Feature Importance (LIME Explanation)
<img width="981" height="378" alt="Image" src="https://github.com/user-attachments/assets/a2894a83-4e9a-4eb8-bb46-fa961433eed6" />

### ROC Curve (Multi-Class)
<img width="1140" height="701" alt="Image" src="https://github.com/user-attachments/assets/321ff21c-4d76-436f-94e4-13f20a3e094a" />

## Notes
- Data is anonymised and used for learning purposes.
- Large raw data files are listed in `.gitignore`. If needed, you can keep a light sample (e.g., 100 rows) inside `data/` for demo purposes.

## Contact
Archee Mewara · LinkedIn: <add-link> · Email: <add email>
