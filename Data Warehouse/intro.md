# Data Warehouse — Introduction

> *A curated collection of completed, publication-ready exploratory data analyses built in Google Colaboratory with Python.*

---

## What Is the Data Warehouse?

In this repository, the **Data Warehouse** is the final destination — the home for fully completed, polished notebooks that have moved past exploration and into finished, presentable analysis.

Where the Data Lake holds raw files and works in progress, the Data Warehouse holds only what is **done**. Every notebook here has been cleaned up, annotated, and is ready to be read, shared, or presented.

---

## What Makes a Notebook "Warehouse-Ready"?

A notebook earns its place in the warehouse when it meets these standards:

- ✅ Analysis is complete and conclusions are clearly stated
- ✅ Code is clean, commented, and runs top to bottom without errors
- ✅ Visualizations are polished and properly labeled
- ✅ Data source and methodology are documented
- ✅ Output is reproducible in Google Colab

---

## Tooling & Environment

All warehouse notebooks are developed in **Google Colaboratory** using the Python data science stack:

| Tool | Role |
|------|------|
| `Pandas` | Data loading, cleaning, reshaping, and aggregation |
| `NumPy` | Numerical operations and array manipulation |
| `Matplotlib` | Core charting and custom figure composition |
| `Seaborn` | Statistical visualizations and styled plots |
| `Plotly` | Interactive charts where applicable |
| `SQL / SQLite` | Structured querying and lightweight persistence |

---

## Completed Analyses

| Notebook | Domain | Tools |
|----------|--------|-------|
| `CO2_global_emission_Project_fall25.ipynb` | Environmental Science | Pandas, Matplotlib, Seaborn |
| `HIV_AIDS_Diagnosis_Project.ipynb` | Public Health | Pandas, Matplotlib, Seaborn |
| `Titanic_Data_Project.ipynb` | Structured Data Analysis | Pandas, Matplotlib, Seaborn |
| Women's Wellbeing Dashboard | Social & Economic Health | Python, SQL, Tableau |
| Running Performance Dashboard | Personal Analytics | Pandas, Streamlit, SQLite |

---

## Visualization Standards

All warehouse notebooks follow a consistent visual style for a cohesive, professional look:

```python
import matplotlib.pyplot as plt
import seaborn as sns

sns.set_theme(style="whitegrid", palette="muted")
plt.rcParams["figure.figsize"] = (12, 6)
plt.rcParams["axes.titlesize"] = 14
```

---

## Related

- [`/Data Lake`](../Data%20Lake/intro.md) — Raw ingestion, staging, and curated datasets
- [`/notebooks`](../notebooks/) — Active and in-progress notebooks
- [Repository README](../README.md) — Full project overview

---

*Part of the [EDAS-lakehouse-repo](https://github.com/AOngomefen/EDAS-lakehouse-repo) maintained by [Andrea Ongomefen](https://linkedin.com/in/andreaongomefen).*
