# Consumer Preference Analytics — Beer Review Analysis

Large-scale behavioral analytics project analyzing 1.5 million beer reviews to uncover consumer preference patterns, segment reviewers, and identify geographic trends. Combines EDA, clustering, and interactive Tableau dashboards to turn raw review data into actionable insights for product and marketing strategy.

---

## Business Problem

Understanding what drives consumer preferences at scale is a core challenge for any product or e-commerce business. This project uses a large public dataset of craft beer reviews as a proxy for that problem — the same analytical approaches apply to product ratings, app reviews, or customer feedback in any industry.

**Key questions answered:**
- What attributes (aroma, taste, appearance, palate) most influence overall ratings?
- Can we segment reviewers into meaningful behavioral groups?
- Are there geographic patterns in beer preferences and brewery performance?
- Which beer styles consistently outperform across reviewer segments?

---

## Key Findings

- **Taste and palate are the strongest drivers** of overall ratings — appearance has the least influence
- **3 distinct reviewer segments** identified via clustering: casual raters, enthusiast reviewers, and power users with significantly higher review volume and consistency
- **Geographic enrichment** (via Google Places API) revealed regional preference patterns — certain styles dominate in specific markets
- **IPAs and Stouts** maintain the highest average ratings across all reviewer segments
- **High-ABV beers** correlate with higher taste ratings but lower palate scores

---

## Techniques Used

- **Exploratory Data Analysis** — rating distributions, correlation analysis, review volume trends
- **Clustering** — KMeans segmentation of reviewers by behavior and preference profile
- **Geographic Enrichment** — brewery latitude/longitude via Google Places API to enable spatial analysis
- **Interactive Dashboard** — Tableau dashboard with cluster analysis and geographic visualization
- **Feature Analysis** — correlations between aroma, taste, appearance, palate, and overall score

---

## Stack

`Python` · `Pandas` · `NumPy` · `scikit-learn` · `Plotly` · `Matplotlib` · `Seaborn` · `Tableau` · `Google Places API`

---

## Files

| File/Folder | Description |
|---|---|
| `cse6242_project_code.ipynb` | Full analysis notebook — EDA, clustering, feature analysis |
| `geo_enrichment/` | Scripts for Google Places API brewery geocoding |
| `visualization/` | Tableau dashboard files |
| `docs/` | Project documentation and final report |

---

## Interactive Dashboard

The Tableau dashboard includes an interactive cluster analysis tab with geographic brewery mapping. To explore it:

1. Download the geo-enriched dataset: [beer\_reviews\_with\_coordinates.csv](https://www.dropbox.com/scl/fi/e6w6tyeh9ya030ovtla6g/beer_reviews_with_coordinates.csv?rlkey=p59f9axioxvthu8k63a1o8wlm&dl=1)
2. Open the Tableau file from the `visualization/` folder
3. Navigate to the **Cluster Analysis** tab

---

## Dataset

1.5M beer reviews from [Kaggle — Beer Reviews](https://www.kaggle.com/datasets/rdoume/beerreviews), enriched with brewery geographic coordinates via the Google Places API.

---

## Context

Completed for CSE 6242: Data & Visual Analytics at Georgia Tech (MS Analytics, Spring 2024). Group project — my contributions spanned all aspects of the analysis, data enrichment pipeline, and visual storytelling.

---

## About

Built by **Ramon Benavides** — analytics professional with nearly 3 years of experience building data pipelines, forecasting models, and decision-support systems.

- [Portfolio](https://ramonbenavidesb98.github.io)
- [LinkedIn](https://linkedin.com/in/ramonbenavides)
- [GitHub](https://github.com/ramonbenavidesb98)
