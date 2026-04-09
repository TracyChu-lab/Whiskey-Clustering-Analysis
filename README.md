# Whiskey-Clustering-Analysis

📌 Overview

This project explores the use of unsupervised learning to identify natural groupings among Scotch whiskies based on their characteristics. Using techniques from Data Science for Business, we apply both Hierarchical Clustering and KMeans Clustering to analyze similarity patterns in the dataset.

The goal is not prediction, but exploration—to understand whether meaningful clusters exist and which method better captures the structure of the data.

⸻

📂 Project Structure
	•	code.ipynb – Main notebook containing data cleaning, clustering, and visualizations
	•	scotch.csv – Dataset of whisky characteristics
	•	quiz.py – Supporting Python script (if applicable)
	•	README.md – Project description and instructions

⸻

📊 Dataset

The dataset contains Scotch whiskies described by:
	•	Binary features (0/1): color, aroma, flavor, finish, etc.
	•	Numeric features: age, score, percentage
	•	Categorical info: name, region (used for reference only)

Most features are binary indicators, making the data high-dimensional and sparse.

⸻

⚙️ Methodology

1. Data Preparation
	•	Removed duplicate and irrelevant columns
	•	Dropped text variables (NAME, DISTRICT) for clustering
	•	Excluded region variables to focus on intrinsic characteristics
	•	Converted all features to numeric
	•	Handled missing values
	•	Standardized features using StandardScaler

⸻

2. Hierarchical Clustering
	•	Applied Ward linkage
	•	Visualized results using a dendrogram
	•	Explored cluster structure at different levels
	•	Extracted clusters using AgglomerativeClustering

👉 Strength: reveals the full similarity structure and local groupings

⸻

3. KMeans Clustering
	•	Used Elbow Method and Silhouette Score to choose k
	•	Best score found at k = 2
	•	Tested k = 4 for comparison
	•	Visualized clusters using PCA (2D projection)

👉 Weakness: assumes well-separated, spherical clusters

⸻

📈 Results
	•	KMeans performed poorly
	•	Low silhouette scores
	•	Strong overlap in PCA plots
	•	Clusters not well separated
	•	Hierarchical clustering performed better
	•	Clear local groupings in dendrogram
	•	More flexible interpretation
	•	Better suited for exploratory analysis

⸻

🧠 Key Insight

The whisky dataset does not exhibit strong global cluster structure, making centroid-based methods like KMeans less effective.

👉 Hierarchical clustering is more appropriate, as it captures similarity relationships without forcing rigid cluster boundaries.

⸻

▶️ How to Run
	1.	Open the notebook in Google Colab or Jupyter
	2.	Upload or mount the dataset (scotch.csv)
	3.	Run cells sequentially

⸻

📚 Reference

Foster, Provost, & Fawcett. Data Science for Business, Chapter 6 (Clustering)

⸻

✨ Author Note

This project focuses on exploratory data analysis using clustering, emphasizing interpretation over prediction and highlighting the importance of choosing methods aligned with data structure.
