# Raw Data Package — Machine Learning-Based Identification of Non-Standard Audit Opinions

Companion data package for the manuscript "Value positioning and policy choices of machine
learning-based identification of non-standard audit opinions: Correcting split-protocol and
scale confounding" (Jinkui He et al.). Compiled 2026-10-26.

## Contents

| Folder | File | Description | Used in |
|---|---|---|---|
| 01_turkish_audit_opinions | financial_data.csv | Raw Kaggle dataset "Audit opinions of Turkish Public Companies" (agrafintech), 27,298 rows x 53 columns, mixed reporting periods, UTF-8-BOM | Tables 1-9, Figs. 1-3 (Turkey) |
| 02_world_bank_cpi_turkey | cpi_turkey.json | World Bank CPI series FP.CPI.TOTL, Turkey (2010=100) | Constant-price deflation (Sect. 3.2, Table 8) |
| 03_us_misstatement_benchmark_jar2020 | data_FraudDetection_JAR2020.csv | Public US misstatement benchmark of Bao, Ke, Li, Yu & Zhang (2020, JAR), 146,045 rows x 46 columns, 1990-2014, 964 positives (0.66%) | Tables 10-11 (Sect. 6) |
| 04_processed_modeling_sample_turkey | model_sample.csv | Final Turkish modeling sample after Table 1 screening and constant-price deflation: 5,100 firm-years, 526 companies, 549 non-standard opinions (10.76%) | All Turkey experiments |

Column dictionaries: see COLUMN_DICTIONARY.md in folders 01 and 03.

## Licenses and provenance

- Dataset 01: Kaggle, license CC BY-NC-SA 4.0 (third-party compilation of BIST periodic disclosures).
- Dataset 02: World Bank Open Data (CC BY 4.0), https://data.worldbank.org, series FP.CPI.TOTL.
- Dataset 03: public release accompanying Bao et al. (2020), https://github.com/JarFraud/FraudDetection.
- Folder 04: derived from 01+02 by the authors' scripted pipeline.

## Integrity

MD5 checksums for every file: md5_checksums.json.

## Reproducibility

All paper numbers were produced by a scripted, seeded (seed = 42) pipeline with preprocessing
statistics fitted inside training folds only. Entry points: audit_pipeline.py (Turkey) and
us_market.py (US). The pipeline code is available from the corresponding author
(hejinkui@ytbu.edu.cn) upon reasonable request.
