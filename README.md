# Customer Segmentation with K-Means Clustering

This project demonstrates a classic unsupervised machine learning workflow to segment customers based on their purchasing behavior. The goal is to uncover hidden patterns in customer data that can be used for targeted marketing strategies.

## Project Overview

The project follows a standard unsupervised learning pipeline:

  - **Problem Definition:** Understanding the business problem of customer segmentation.
  - **Data Exploration:** Selecting key features for analysis.
  - **Algorithm Selection:** Choosing an appropriate clustering algorithm.
  - **Optimal Cluster Determination:** Using the Elbow Method to find the best number of clusters.
  - **Clustering & Visualization:** Applying the algorithm and visualizing the results.

## The Dataset

The dataset used in this project is `Mall_Customers.csv`, containing information about customers from a shopping mall. For this analysis, I focused on two key features:

  - **`Annual Income (k$)`**: The customer's annual income in thousands of dollars.
  - **`Spending Score (1-100)`**: A score assigned to the customer based on their spending behavior.

The goal is to discover meaningful groups within the customer base using these two features.

## Methodology

### 1\. Data Preparation

I intentionally selected only the `Annual Income` and `Spending Score` features to enable **2D visualization** of the clusters. This approach makes the results highly interpretable and easy to present.

### 2\. Choosing the Right Algorithm

Since the dataset did not have predefined labels or categories for the customers, this is an **unsupervised learning** problem. The **K-Means** algorithm was chosen for its simplicity, efficiency, and widespread use in customer segmentation tasks.

### 3\. Finding the Optimal Number of Clusters

A key challenge in K-Means is determining the optimal number of clusters (`k`). I addressed this using the **Elbow Method**. By plotting the **WCSS (Within-Cluster Sum of Squares)** for a range of `k` values, a clear "elbow" point emerged at `k=5`, indicating that 5 is the optimal number of clusters for this dataset.

### 4\. Clustering and Analysis

The K-Means algorithm was then applied with `k=5` to group the customers. The results were visualized on a scatter plot, showing five distinct clusters. Each cluster represents a different customer segment based on their income and spending habits, such as:

  - **Cluster 1 (Top-Right):** High-income, high-spending customers (the "Super Spenders").
  - **Cluster 2 (Bottom-Left):** Low-income, low-spending customers (the "Frugal").
  - **Cluster 3 (Center):** Average-income, average-spending customers.

By identifying these segments, a marketing team can design highly targeted and effective campaigns for each group.

## Installation

To run this project, you need the following libraries:

  - `numpy`
  - `pandas`
  - `scikit-learn`
  - `matplotlib`

You can install them using pip:

```sh
pip install numpy pandas scikit-learn matplotlib
```

## How to Run

1.  Clone this repository:
    ```sh
    git clone https://github.com/Amir-Sa02/Customer-Segmentation-with-K-Means-Clustering.git
    ```
2.  Navigate to the project directory:
    ```sh
    cd Customer-Segmentation-with-K-Means-Clustering
    ```
3.  Run the Jupyter Notebook or the Python script containing the code.
    ```sh
    jupyter notebook mall-customers-clustering.ipynb
    ```
