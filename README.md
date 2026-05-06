# EDAS · Lakehouse Repository

> *Exploratory Data Analysis, curated datasets, and reproducible research artifacts — organized as a personal data lakehouse.*

**Owner:** [AOngomefen](https://github.com/AOngomefen) &nbsp;|&nbsp; **Stack:** Python · SQL · Pandas · NumPy · Matplotlib · Tableau · Streamlit · Jupyter

---

## Overview

This repository is a living collection of data analysis projects, course assignments, and independent research. It functions as a lightweight **data lakehouse** — a single, governed source of truth for raw ingestion, staged transformations, and curated, analysis-ready datasets.

Projects span public health, environmental science, and personal performance analytics, built with a consistent emphasis on **reproducibility**, **clean data governance**, and **clear visual storytelling**.

---

## Projects

### Women's Wellbeing Data Dashboard
`Python · SQL · Tableau · Pandas`

Analyzed national and sub-national women's well-being data sourced from public health and economic databases. Cleaned and modeled complex, multi-dimensional datasets using Python and SQL, then designed an interactive **Tableau dashboard** visualizing key indicators across health, economic empowerment, and social equity dimensions.

---

### Running Performance Dashboard
`Python · Streamlit · Pandas · SQLite`

An end-to-end personal analytics application tracking pace, distance, heart rate, and VO₂ max over time. Performance logs are managed with **Pandas** and persisted in **SQLite**, with a clean **Streamlit** interface built around user-focused visualizations and trend analysis.

---

### CO₂ Global Emissions Analysis
`Python · Pandas · Matplotlib`
📄 `CO2_global_emission_Project_fall25.ipynb` · `co2_global_emissions_lab_clean.csv`

Explored global CO₂ emission trends using cleaned time-series data. Applied exploratory analysis techniques to identify regional patterns, per-capita emission disparities, and longitudinal trends across the industrial era.

---

### HIV/AIDS Diagnoses — Neighborhood, Sex & Race/Ethnicity
`Python · Pandas · Matplotlib`
📄 `HIV_AIDS_Diagnosis_Project.ipynb` · `HIV_AIDS_Diagnoses_by_Neighborhood_Sex_and_Race_Ethnicity.csv`

A public health EDA examining HIV/AIDS diagnosis rates segmented by neighborhood, sex, and race/ethnicity. Analysis surfaces disparities across demographic groups and geographies to support data-informed public health understanding.

---

### Titanic Survival Analysis
`Python · Pandas · Matplotlib`
📄 `Titanic_Data_Project.ipynb`

Classic structured data project exploring survival patterns on the Titanic. Covers data cleaning, feature analysis, demographic breakdowns, and visualization of survival rates across passenger class, age, and sex.

---

## Reference Modules

The following files are **reference and utility notebooks** currently being cleaned and organized as part of an ongoing repository restructure. They contain reusable patterns, experimental code, and foundational exercises.

| File | Description |
|------|-------------|
| `ref0.md` | Markdown reference and formatting exercises |
| `ref1.ipynb` | Reference notebook — utility patterns and exploratory snippets |
| `ref2.ipynb` | Reference notebook — data wrangling and cleaning techniques |
| `ref3.ipynb` | Reference notebook — visualization and analysis experiments |

> **Note:** These modules are actively being refactored. Content may be reorganized into `src/` or `notebooks/` as the lakehouse structure matures.

---

## Repository Structure

```
EDAS-lakehouse-repo/
├── data/
│   ├── raw/          # Source files — do NOT commit sensitive or large raw data
│   ├── staging/      # Working files used during cleaning and transformation
│   ├── curated/      # Cleaned, documented datasets cleared for inclusion
│   └── metadata/     # Schemas, provenance notes, per-dataset READMEs
├── notebooks/        # Jupyter notebooks (.ipynb)
├── src/              # Reusable code and helper modules
├── docs/             # Documentation, access instructions, slides
├── assignments/      # Course assignments and starter code
├── .github/          # Issue templates, Actions, PR templates
├── README.md
├── .gitignore
└── requirements.txt
```

---

## Getting Started

```bash
# Clone the repository
git clone https://github.com/AOngomefen/EDAS-lakehouse-repo.git
cd EDAS-lakehouse-repo

# Create and activate a virtual environment
python -m venv .venv
source .venv/bin/activate        # macOS / Linux
.venv\Scripts\activate           # Windows

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter Lab
jupyter lab
```

---

## Data Governance

This repository follows strict data handling practices:

- **No PII or sensitive records** are committed to the public repository
- Restricted datasets are represented by anonymized or synthetic samples only
- Each dataset in `data/curated/` includes a provenance `README.md`
- Access requests for restricted data are handled externally and tracked via Issues

**Pre-commit checklist:**

- [ ] Is the data anonymized or synthetic?
- [ ] Is the data cleared for public distribution?
- [ ] Is provenance and metadata documented?

---

## Environment & Reproducibility

Dependencies are pinned in `requirements.txt`. Notebooks use small, included sample datasets for full reproducibility. Where larger datasets are required, download instructions and graceful skip logic are embedded directly in the notebook.

---

## License & Attribution

Code in this repository is available under the **MIT License**. Dataset-specific licenses and citation instructions are documented in `data/<dataset>/README.md` for each included source.

---

## Contact

**Andrea Ongomefen**
[github.com/AOngomefen](https://github.com/AOngomefen) · [linkedin.com/in/andreaongomefen](https://linkedin.com/in/andreaongomefen)
