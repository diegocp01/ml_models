# LAPD Crime ML Models — Diego Cabezas

**Data science thesis / portfolio study** predicting whether an LAPD crime report looks *violent* or *non-violent*, using public Los Angeles crime data (roughly **2020–2024**).

> **Start here if you’re not a Python person:**  
> **[Friendly study explainer (open in browser)](docs/study-explained.html)** — plain-English summary of the question, data, pipeline, and verified results.

## Results teaser (from the saved notebook)

| Model | Accuracy | Notes |
| --- | --- | --- |
| **Random Forest** (`n_estimators=100`) | **~87.6%** | Best overall; violent-class F1 ≈ **0.69** |
| Neural net (Keras MLP) | **val ≈ 87.4%** | Close to the forest on overall accuracy |
| Logistic Regression | **~81.9%** | Strong on non-violent; weak violent recall (~0.20) |

Unsupervised (2024 subset): K-Means silhouette **0.554** vs DBSCAN **0.443** on UMAP embeddings.

Full tables, caveats, and how to read the notebook: **[docs/study-explained.html](docs/study-explained.html)**.

## Source of truth

- Notebook: [`LAPD_Crime_ML_Models.ipynb`](LAPD_Crime_ML_Models.ipynb)
- **This docs pass did not change the notebook.** The `.ipynb` remains the canonical code + metrics source.

## Links

- [Open in Colab](https://colab.research.google.com/drive/1vkykqjNrHV5SSGEM-k_7C6TxBbrptioj?usp=sharing) (optional — run in the browser)
- [Presentation](https://www.canva.com/design/DAGMtxvrRMs/dgT1HW1OBnttIUw1G9WhyQ/edit?utm_content=DAGMtxvrRMs&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)
- [LAPD Crime Data (City of LA)](https://data.lacity.org/Public-Safety/Crime-Data-from-2020-to-Present/2nrs-mtv8)

## What’s inside the study

1. Clean & explore ~**963k** public incident rows  
2. Build a violent / non-violent label and engineered time/area/victim/weapon features  
3. Unsupervised structure discovery on the **2024** slice (PCA, UMAP, K-Means, DBSCAN)  
4. Supervised models + a small deep-learning network  
5. Interactive prediction playgrounds in the notebook  

## Author

Diego Cabezas — data science thesis / portfolio piece.
