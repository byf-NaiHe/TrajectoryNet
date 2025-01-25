# TrajectoryNet Tutorial: Unveiling the Mysteries of Cell Fate

## Introduction

In this repository, I use **TrajectoryNet** and **PHATE** to analyze a time-series dataset of 31,000 human embryonic stem cells (EB) over a 27-day differentiation period. Through this repository, I gain insights into inferring cell differentiation trajectories and visualizing the dynamic changes in cell fate using single-cell RNA sequencing data.

### Citations
- **TrajectoryNet**: Tong, A., Huang, J., Wolf, G., van Dijk, D. & Krishnaswamy, S. TrajectoryNet: A Dynamic Optimal Transport Network for Modeling Cellular Dynamics. in Proceedings of the 37th International Conference on Machine Learning (2020). [Paper Link](http://proceedings.mlr.press/v119/tong20a/tong20a.pdf)
- **PHATE**: Moon, K. R. et al. Visualizing structure and transitions in high-dimensional biological data. Nature Biotechnology 37, 1482–1492 (2019). [Paper Link](https://doi.org/10.1038/s41587-019-0336-3)

## Dataset

The dataset used is sourced from the publicly available **Mendeley Dataset**, which contains a time-series of 31,000 cells over 27 days of differentiation. The dataset includes five time points, with cells analyzed using single-cell RNA sequencing technology (10x Genomics).

### Dataset Structure
```
download_path
└── scRNAseq
    ├── scRNAseq.zip
    ├── T0_1A
    │   ├── barcodes.tsv
    │   ├── genes.tsv
    │   └── matrix.mtx
    ├── T2_3B
    │   ├── barcodes.tsv
    │   ├── genes.tsv
    │   └── matrix.mtx
    ├── T4_5C
    │   ├── barcodes.tsv
    │   ├── genes.tsv
    │   └── matrix.mtx
    ├── T6_7D
    │   ├── barcodes.tsv
    │   ├── genes.tsv
    │   └── matrix.mtx
    └── T8_9E
        ├── barcodes.tsv
        ├── genes.tsv
        └── matrix.mtx
```

## Analysis Steps

1. **Loading 10X Data**  
   - Use the `scprep` package to load 10X single-cell RNA sequencing data.
   - Merge datasets from different time points and create a time-series vector.

2. **Data Preprocessing**  
   - Filter low-expression genes and dead cells.
   - Normalize and transform the data (e.g., square root transformation).

3. **Embedding Data with PHATE**  
   - Use the PHATE algorithm to reduce the dimensionality of high-dimensional single-cell data and generate 2D or 3D visual embeddings.

4. **Modeling Cell Dynamics with TrajectoryNet**  
   - Use TrajectoryNet to infer cell differentiation trajectories.
   - Visualize dynamic changes in gene space.

## References

1. Tong, A., Huang, J., Wolf, G., van Dijk, D. & Krishnaswamy, S. TrajectoryNet: A Dynamic Optimal Transport Network for Modeling Cellular Dynamics. in Proceedings of the 37th International Conference on Machine Learning (2020). 
2. Moon, K. R. et al. Visualizing structure and transitions in high-dimensional biological data. Nature Biotechnology 37, 1482–1492 (2019). 
