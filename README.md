#Problem Statement 1 - Google Play Sentiment Classification & App Recommendation

## Objective

Classify the sentiment of user reviews on Google Play apps and recommend the top-rated apps based on positive sentiment and helpfulness scores.
------
## 🗃️ Dataset
- **apps_reviews.csv** – Reviews with text, score, and helpfulness.
- **apps_info.csv** – Metadata about apps (name, category, etc.)

---------
.....***Methodology***...
1. Data Preprocessing 
	1. Removed all instances where data was missing 
	2.Removed any reviews that were shorter than 10 characters
2. Sentiment Labels 
	1. For each review, labelled as `positive`, `neutral`, or `negative` based on review score 
3. Text Vectorization 
 1.Utilized TF-IDF to change the textual representation of the review to a numeric representation 
4. Train the Classifier 
 1.Classifier type: `Logistic Regression` trained on tagged reviews 
5. Model Measure 
	- Accurate: ~86% 
	- F1-score (positive): ~ 0.91 
6. Recommendation Engine 
	- Top 10 apps are determined based on number of positive reviews + number of total helpful votes

## How to Run

1. Clone this repository
2. Ensure the following files are in place:
   - `apps_reviews.csv`
   - `apps_info.csv`
3. Open and run `GooglePlay_Sentiment_Recommendation.ipynb` in Jupyter or VS Code

---

## 📁 Files

| File                             | Description                          |
|----------------------------------|--------------------------------------|
| `GooglePlay_Sentiment_Recommendation.ipynb` | Main notebook with code |
| `recommended_apps.csv`          | Output of top recommended apps       |
| `data/apps_reviews.csv`         | Raw review data                      |
| `data/apps_info.csv`            | Raw app metadata                     |

## Author
This project was submitted as part of the Synapse Sprint .
created by
-Shreyan Das
