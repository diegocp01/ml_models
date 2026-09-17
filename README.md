# LAPD Crime ML Models (thesis)

Predict whether an Los Angeles crime record is **violent** or **non-violent** using public LAPD data (2020 → mid-2024). Supervised models + unsupervised exploration + a small deep-learning net — documented for both technical and non-technical readers.

## Start here (no Python required)

**[Study explained in plain English →](docs/study-explained.html)**  
Single-file HTML: what the notebook does, what data it used, and **verified results only**.

## Verified results teaser

From `LAPD_Crime_ML_Models.ipynb` (not invented):

| Model | Overall accuracy | Violent-class highlight |
| --- | --- | --- |
| Logistic Regression | **81.99%** | F1 **0.30** (recall 0.20) |
| Random Forest (100 trees) | **87.67%** | F1 **0.70** (recall 0.75) |
| Random Forest (50 trees) | **87.59%** | F1 **0.69** |
| Keras neural net | **87.39%** validation accuracy | class-wise metrics not tabled in notebook |

- Rows in the notebook fetch: **963,006**
- Data window stated in notebook: **01/01/2020 – 08/01/2024**
- Best classical pick in the write-up: **Random Forest** (stronger violent-crime detection than logistic regression)

## Notebook & links

- Notebook in this repo: `LAPD_Crime_ML_Models.ipynb` (same content as the working Colab)
- [Open in Colab](https://colab.research.google.com/drive/1vkykqjNrHV5SSGEM-k_7C6TxBbrptioj?usp=sharing)
- [Presentation](https://www.canva.com/design/DAGMtxvrRMs/dgT1HW1OBnttIUw1G9WhyQ/edit?utm_content=DAGMtxvrRMs&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)

## What’s inside the study

1. **Data** — LAPD “Crime Data from 2020 to Present” (~1M-scale public table; notebook run logged 963,006 rows).
2. **Target** — `violent_crime` (1 / 0) from crime characteristics.
3. **Features** — area, victim age/sex/descent, weapon description, year/month/day/hour.
4. **Models** — Logistic Regression, Random Forest (with a small `n_estimators` check), Keras binary net.
5. **Extras** — EDA, 2024-only unsupervised pass, interactive prediction playground.

## Audit note

Claims in `docs/study-explained.html` and this README are limited to numbers/findings that appear in the notebook markdown or cell outputs. Deep-learning **class-wise** precision/recall are omitted because the notebook does not table them.
