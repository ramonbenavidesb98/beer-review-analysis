# beer-review-analysis
# Beer Review Analysis

This project analyzes over 1.5 million beer reviews to uncover insights about consumer preferences, beer styles, and reviewer behavior. It was completed as part of the CSE 6242 course at Georgia Tech.

- Objective
Explore trends and patterns in beer reviews.

Analyze beer styles, average scores, and user behaviors.

Identify which beers and reviewers stand out across categories.

Build visualizations to support exploratory insights.

- Technologies Used
Python

Pandas, NumPy

Matplotlib, Seaborn

Scikit-learn

Jupyter Notebook

- Dataset
The dataset was sourced from Kaggle: Beer Reviews Dataset

To download programmatically:

python
Copy
Edit
import kagglehub
path = kagglehub.dataset_download("rdoume/beerreviews")
- Key Analyses
Beer Style Distribution
Examined which styles are most reviewed and their average ratings.

Rating Breakdown
Explored how appearance, aroma, palate, and taste contribute to the overall score.

Top Beers by Rating
Identified the highest-rated beers with a minimum number of reviews.

User Behavior
Found users with the most reviews and analyzed their rating trends.

Correlation Heatmaps
Measured how review categories relate to overall scores.

Dimensionality Reduction
Applied PCA and clustering to detect hidden groupings in the data.

- How to Run
Install dependencies:

nginx
Copy
Edit
pip install pandas numpy matplotlib seaborn scikit-learn kagglehub
Download the dataset (see dataset section above).

Run cse6242_project_code.ipynb in Jupyter Notebook or VS Code.

- Author's Note
This project was completed as part of Georgia Tech’s MS Analytics program. It demonstrates a blend of data wrangling, EDA, statistical exploration, and visual storytelling—skills applicable to data science and marketing analytics roles.
