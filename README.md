# Customer-Segmentation-Analysis

This project dives into customer segmentation analysis using the IFood dataset, aiming to uncover distinct customer groups for targeted marketing strategies.

## Project Overview

The analysis follows a structured approach:

1. **Data Preparation:**
   - The IFood dataset is retrieved from a GitHub repository and loaded into a Pandas DataFrame.
   - Data cleaning involves handling missing values and removing irrelevant columns.
   - Outliers in the 'MntTotal' (total spending) column are addressed using the Interquartile Range (IQR) method to ensure data quality.

2. **Exploratory Data Analysis (EDA):**
   - EDA techniques are employed to gain insights into the dataset:
     - Distribution of key variables like 'Income' and 'Age' is visualized using histograms and box plots.
     - Skewness and kurtosis of the 'Age' variable are calculated to understand its distribution characteristics.
     - Correlations between 'MntTotal' and demographic features are explored to identify potential relationships.
     - Point-biserial correlation analysis assesses the association between categorical variables (e.g., 'Marital', 'Education') and 'MntTotal'.

3. **Feature Engineering:**
   - New features are engineered to enhance the analysis:
     - A 'Marital' feature is created by consolidating one-hot encoded marital status columns.
     - An 'In_relationship' feature is derived based on marital status, indicating whether a customer is in a relationship.

4. **Clustering with K-means:**
   - Relevant features for clustering are selected, including 'Income', 'MntTotal', and 'In_relationship'.
   - StandardScaler is applied to standardize these features, ensuring they contribute equally to the clustering process.
   - Principal Component Analysis (PCA) reduces dimensionality to two components for visualization purposes.
   - The optimal number of clusters is determined using the elbow method (assessing inertia) and silhouette score (evaluating cluster separation).
   - K-means clustering is performed with the chosen number of clusters to group customers based on their characteristics.

5. **Cluster Analysis and Interpretation:**
   - The clustered data is visualized using a scatter plot of the principal components, revealing the distinct groups.
   - Mean values of key features are analyzed for each cluster to understand their defining characteristics.
   - Product consumption patterns are compared across clusters using a bar plot, highlighting preferences within each group.
   - Cluster sizes and their proportions are examined to assess their relative importance.
   - The relationship between 'Income', 'MntTotal', and 'In_relationship' is investigated within each cluster, providing insights into spending behavior and demographics.

## Key Findings and Implications

- The analysis successfully identifies distinct customer segments within the IFood dataset.
- Each cluster exhibits unique characteristics in terms of income, spending patterns, and relationship status.
- These insights can be leveraged for targeted marketing campaigns:
   - Tailored offers and promotions can be designed for each cluster based on their preferences.
   - Communication strategies can be customized to resonate with specific customer groups.
- This segmentation analysis enables IFood to enhance customer relationship management and optimize marketing efforts.

## How to Use This Repository

1. Clone the repository.
2. Install the required libraries (NumPy, Pandas, Seaborn, Matplotlib, Scikit-learn).
3. Run the Jupyter Notebook to reproduce the analysis.

## Future Work

- Explore additional clustering algorithms (e.g., hierarchical clustering, DBSCAN) to compare results.
- Incorporate more features into the clustering process to capture a wider range of customer attributes.
- Develop predictive models to identify potential high-value customers or predict churn.
