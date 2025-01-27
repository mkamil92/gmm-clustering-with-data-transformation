# Improving GMM Clustering with Data Transformation

This repository demonstrates how **Gaussian Mixture Model (GMM)** clustering can be improved by applying statistical transformations to datasets. The project compares the performance of GMM clustering on two datasets before and after applying the **Yeo-Johnson Transformation**, a technique for normalizing skewed data. The transformed data yielded significantly better clustering results in both cases.

---

## Datasets

### 1. Obesity Dataset:
- **Description**: Contains demographic and health-related attributes for obesity classification.

### 2. Student Dataset:
- **Description**: Contains academic and behavioral data of students to analyze clusters based on their performance.
---

## Objective
- To apply **GMM Clustering** on both datasets and evaluate its performance on the **original data**.
- To apply the **Yeo-Johnson Transformation** to the datasets and evaluate the performance of GMM clustering on the **transformed data**.
- To demonstrate how statistical transformations can enhance clustering results by improving the distribution of data.

---

## Workflow

### 1. Data Preprocessing
- **Handle Missing Values**: Imputed missing values with mean/mode as needed.
- **Scaling**: Standardized features using `StandardScaler`.
- **Exploration**: Performed Exploratory Data Analysis (EDA) to examine feature distributions and identify skewness.

### 2. Clustering with Original Data
- Applied **GMM Clustering** with:
  - Optimal number of clusters determined using metrics like **BIC (Bayesian Information Criterion)** and **Silhouette Score**.
  - Visualized clusters using **PCA** and **t-SNE** for dimensionality reduction.
- Evaluated clustering performance with metrics:
  - Silhouette Score
  - Adjusted Rand Index (ARI)

### 3. Data Transformation
- Applied the **Yeo-Johnson Transformation** to address skewed feature distributions.
- Repeated clustering methodology on the transformed data.

### 4. Clustering with Transformed Data
- Reapplied GMM clustering using the transformed dataset.
- Evaluated clustering performance with the same metrics.
- Compared results with the original GMM clustering.

---

## Results and Insights

### 1. Obesity Dataset:
- **Original GMM**:
  - Silhouette Score: 0.138
  - Clusters were imbalanced and did not clearly represent obesity categories.
- **Transformed Data with Yeo-Johnson**:
  - Silhouette Score: 0.527 (Improved)
  - Clusters were more balanced and better aligned with obesity levels.

### 2. Student Dataset:
- **Original GMM**:
  - Silhouette Score: 0.1433
  - Clusters did not align well with academic performance and behavioral features.
- **Transformed Data with Yeo-Johnson**:
  - Silhouette Score: 0.5140 (Improved)
  - Clearer separation of clusters based on performance and participation metrics.

### Key Observations:
- The **Yeo-Johnson Transformation** effectively normalized skewed data, improving the performance of GMM.
- Transformed data led to more meaningful and interpretable clusters in both datasets.
