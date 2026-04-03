# Customer Clustering with KMeans

This project implements a customer segmentation solution using the **KMeans clustering** algorithm. The goal is to group customers based on their annual income and spending score, enabling businesses to better understand their customer base and tailor marketing strategies accordingly.

## 📁 Project Structure

├── Dokumentacja_UM_L2_48860.pdf   # Project documentation (Polish)
├── Mall_Customers.csv             # Customer dataset
├── Projekt_UM_L2_48860.ipynb      # Jupyter Notebook with full implementation
└── README.md                      # This file

## 🎯 Objective

Perform unsupervised learning to cluster customers into distinct groups using the `Mall_Customers` dataset. The analysis includes:

- Data exploration and visualization
- Feature selection and normalization
- Determining optimal number of clusters (Elbow method)
- Training a KMeans model
- Visualizing clusters and centroids
- Interpreting the results for business insights

## 📊 Dataset

The dataset contains 200 customer records with the following attributes:

- `CustomerID` – Unique identifier
- `Gender` – Male / Female
- `Age` – Customer age
- `Annual Income (k$)` – Yearly income in thousand dollars
- `Spending Score (1-100)` – Score assigned by the mall based on customer behavior

> Only **Annual Income** and **Spending Score** are used for clustering.

## 🧠 Methodology

1. **Import libraries** – pandas, numpy, matplotlib, seaborn, scikit-learn.
2. **Load and explore data** – check for missing values, data types, and basic statistics.
3. **Visualize distributions** – pair plots to understand relationships.
4. **Feature selection** – choose `Annual Income` and `Spending Score`.
5. **Normalization** – use `StandardScaler` to bring features to the same scale.
6. **Elbow method** – compute inertia for k = 1..10 and plot to find optimal k.
7. **Train KMeans** – with optimal k = 5.
8. **Visualize clusters** – scatter plot of clusters and centroids.
9. **Export / interpret** – assign cluster labels to each customer.

## 🔧 Requirements

Install the required Python packages:


pip install pandas numpy matplotlib seaborn scikit-learn


Alternatively, run the notebook in **Google Colab** – all libraries are pre-installed.

## 🚀 How to Run

1. Clone or download this repository.
2. Open `Projekt_UM_L2_48860.ipynb` in Jupyter Notebook / JupyterLab or upload to Google Colab.
3. Upload the `Mall_Customers.csv` file when prompted.
4. Execute cells sequentially from top to bottom.

## 📈 Results

The elbow plot shows a clear "bend" at **k = 5**, which is chosen as the optimal number of clusters.

The final clustering (after standardization) separates customers into five interpretable segments:

- **Cluster 0** – High income, high spending (top customers)
- **Cluster 1** – Moderate income, moderate spending
- **Cluster 2** – Low income, high spending (aspirational shoppers)
- **Cluster 3** – Moderate income, low spending (cautious spenders)
- **Cluster 4** – Low income, low spending (economy shoppers)

Each cluster can be targeted with specific marketing campaigns.

## 📸 Sample Visualization

The notebook includes a 2D scatter plot of the clusters with centroids marked as yellow X's.

## 📝 Notes

- The algorithm is sensitive to outliers and requires numerical features.
- The number of clusters was determined heuristically using the elbow method.
- The model is trained only on `Annual Income` and `Spending Score` for clear 2D visualization.

## 📚 References

- Scikit-learn documentation: [KMeans](https://scikit-learn.org/stable/modules/clustering.html#k-means)
- Bishop, C.M. – *Pattern Recognition and Machine Learning*

## 👤 Author

**Mikita Kutsayeu**  
Student ID: 48860  
Warsaw, Akademia Vizja – Faculty of Information Technology