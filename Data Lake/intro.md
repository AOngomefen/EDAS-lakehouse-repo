# Data Lake — Introduction

> *A centralized, governed storage layer for raw, staged, and curated data across all analysis projects in this repository.*

---

## What Is a Data Lake?

A **data lake** is a storage architecture that holds large volumes of data in its native format — structured, semi-structured, or unstructured — until it is needed for analysis. Unlike a traditional database, a data lake does not require data to be cleaned or modeled before ingestion. Raw data lands here first, and transformations happen downstream.

This repository's data lake is intentionally lightweight — designed for personal and academic scale — but follows the same organizational principles used in production data engineering environments.

---

## Why a Data Lake?

As the number of projects and datasets in this repository grows, a flat file structure becomes difficult to navigate and reproduce. The data lake solves this by:

- **Centralizing** all datasets under a single, governed directory
- **Separating concerns** between raw ingestion, active transformation, and analysis-ready output
- **Enforcing provenance** — every dataset knows where it came from and what was done to it
- **Protecting sensitive data** — raw files that cannot be published stay out of version control while their metadata and anonymized samples remain accessible

---

## Layer Structure

The data lake is organized into three layers, mirroring the **Bronze → Silver → Gold** pattern common in modern lakehouse architectures:

| Layer | Folder | Purpose |
|-------|--------|---------|
| 🟤 Bronze | `data/raw/` | Raw source files exactly as ingested — never modified |
| ⚪ Silver | `data/staging/` | Cleaned, filtered, and transformed working files |
| 🟡 Gold | `data/curated/` | Analysis-ready datasets cleared for use in notebooks |

A `data/metadata/` directory sits alongside these layers and holds schema definitions, provenance notes, and per-dataset documentation.

---

## Data Currently in the Lake

| Dataset | Source | Layer | Project |
|---------|--------|-------|---------|
| `co2_global_emissions_lab_clean.csv` | Public environmental records | Curated | CO₂ Global Emissions Analysis |
| `HIV_AIDS_Diagnoses_by_Neighborhood_Sex_and_Race_Ethnicity.csv` | NYC Open Data | Curated | HIV/AIDS Diagnoses EDA |
| Running performance logs | Personal export | Staging | Running Performance Dashboard |
| Women's wellbeing indicators | Public health databases | Curated | Women's Wellbeing Dashboard |

---

## Data Governance Principles

All data stored in this lake follows these rules:

1. **Raw data is never overwritten.** Transformations always produce new files in `staging/` or `curated/`.
2. **No PII or sensitive records are committed** to the public repository. Restricted data is represented by anonymized samples or synthetic equivalents.
3. **Every dataset has a metadata file** documenting its source, license, anonymization steps, and permitted uses.
4. **Large files are excluded from version control** via `.gitignore`. Download instructions are embedded in the relevant notebook.

---

## Workflow

```
External Source
      │
      ▼
  data/raw/          ← Ingest raw file as-is
      │
      ▼
  data/staging/      ← Clean, filter, transform
      │
      ▼
  data/curated/      ← Analysis-ready, documented dataset
      │
      ▼
  notebooks/         ← Load curated data → analyze → visualize
```

---

## Related

- [`/notebooks`](../notebooks/) — Jupyter analysis notebooks
- [`/src`](../src/) — Reusable cleaning and transformation scripts
- [`/docs`](../docs/) — Extended documentation and data access instructions
- [Repository README](../README.md) — Full project overview

---

*This data lake is part of the [EDAS-lakehouse-repo](https://github.com/AOngomefen/EDAS-lakehouse-repo) maintained by [Andrea Ongomefen](https://linkedin.com/in/andreaongomefen).*
