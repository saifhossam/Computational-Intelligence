# Dimensionality Reduction for Data Visualization Using Nature-Inspired Algorithms

This project explores traditional and nature-inspired dimensionality reduction techniques to visualize high-dimensional data. It features a GUI for interactive algorithm selection, visualization, and reproducibility testing.

---

**Dataset**

* **Source**: Digits dataset from Scikit-learn
* **Features**: 64 numerical features (8x8 pixel images)
* **Classes**: Digits 0–9
* **Preprocessing**: StandardScaler for normalization

---

**Algorithms Implemented**

| Algorithm           | Description                                      |
| ------------------- | ------------------------------------------------ |
| PCA                 | Linear method preserving global variance         |
| t-SNE               | Non-linear embedding preserving local structure  |
| UMAP                | Topology-preserving manifold learning            |
| ISOMAP              | Graph-based method preserving geodesic distances |
| SOM                 | Neural network for topological self-organization |
| Autoencoder         | Deep learning compression and reconstruction     |
| Autoencoder + t-SNE | Combines AE compression with t-SNE visualization |

---

**Highlights of Algorithms**

* **PCA**: Fast, preserves global structure; limited on non-linear data
* **t-SNE**: Reveals clusters well but lacks reproducibility and global context
* **UMAP**: Faster and more stable than t-SNE; preserves both local/global patterns
* **ISOMAP**: Useful for curved manifolds; sensitive to noise
* **SOM**: Intuitive 2D mapping maintaining topological relations
* **Autoencoder**: Learns non-linear features; useful for high-dimensional data
* **Autoencoder + t-SNE**: Efficient and better noise handling for large data

---

**GUI Functionality**

* Dropdown for algorithm selection
* Dynamic parameter inputs per method
* Buttons for "Run" and "Run 30 Repetitions"
* Embedded matplotlib plot for 2D visualization

---

**Parameter Customization**

| Method      | Key Parameters                            |
| ----------- | ----------------------------------------- |
| PCA         | `n_components`                            |
| t-SNE       | `n_components`, `perplexity`              |
| UMAP        | `n_components`, `n_neighbors`, `min_dist` |
| ISOMAP      | `n_components`, `n_neighbors`             |
| SOM         | `grid_size`, `sigma`, `learning_rate`     |
| Autoencoder | `encoding_dim`, `epochs`, `batch_size`    |
| AE + t-SNE  | Above + `perplexity`                      |

---

**SOM Configuration**

* **Library**: MiniSom
* **Grid**: `grid_size × grid_size`
* **Iterations**: 100
* **Metric**: Euclidean
* **Initialization**: Random

---

**Reproducibility**

* The "Run 30 Repetitions" feature executes the selected algorithm 30 times using different seeds.
* Seeds are saved in `seeds_used.txt` for traceability.

---

**Goal**
To compare dimensionality reduction methods—especially biologically inspired ones—for their effectiveness, efficiency, and consistency in visualizing high-dimensional data.

---
