# Well Log Clustering using KMeans (Unsupervised ML)

This project applies **unsupervised machine learning** to well log data in order to identify geological facies automatically.

The objective is to group subsurface intervals based on petrophysical properties without using labeled data.

---

## Dataset

The dataset contains continuous well log measurements indexed by depth:

- **RHOB** – Bulk Density  
- **GR** – Gamma Ray  
- **NPHI** – Neutron Porosity  
- **PEF** – Photoelectric Effect  
- **DTC** – Sonic Travel Time  

Depth (MD) is used as the natural ordering variable.

---

## Methodology

1. Data cleaning (removal of missing values)
2. Feature standardization using `StandardScaler`
3. Optimal cluster selection using the **Elbow Method**
4. KMeans clustering (k = 3)
5. Cluster interpretation using original log units
6. Principal Component Analysis (PCA) for 2D visualization
7. Silhouette Score evaluation

---

## Results

- Optimal number of clusters: **3**
- Silhouette Score: **0.55** (indicates solid cluster structure)
- PCA retained ~80% of total variance in 2 components

The clustering separated the formation into three lithological facies:

- **Cluster 0** – High-porosity sand  
- **Cluster 1** – Shale interval  
- **Cluster 2** – Dense rock (carbonate or tight sand)

Clusters appear in continuous depth intervals, consistent with geological layering.

---

## Key Concepts Demonstrated

- Distance-based clustering
- Feature scaling importance
- Dimensionality reduction (PCA)
- Cluster validation (Silhouette Score)
- Interpretation of clusters using domain knowledge

---

## Conclusion

KMeans successfully identified meaningful geological patterns in the well log data.  
The clustering aligns with expected lithological layering and demonstrates how unsupervised learning can extract structure from continuous subsurface measurements.

---

**Tools Used:**  
`Python`, `Pandas`, `Scikit-learn`, `Matplotlib`
