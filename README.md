# Scarf workflow 
### scRNA-seq analysis 5K PBMC
[Scarf](https://scarf.readthedocs.io/en/latest/index.html) is a Python package that performs memory-efficient analysis of single-cell genomics data. Using an efficient data chunking process (using Zarr and Dask) Scarf manages to perform the core steps of single-cell genomics data analysis with very low memory consumption. Scarf’s core step is to efficiently generate a neighbourhood graph (KNN graph) of cells. dataset used is 10x genomics 5K PBMC (peripheral blood mononuclear cell)
* Format conversion: convert file into the Zarr format
* Cell filtering: 
* Feature selection: normalize data and identify the highly variable genes
* Graph creation: creating a neighbourhood graph 
* Low dimensional embedding and clustering: calculate UMAP graph
* Cell clustering: clusters identification
* Marker gene identification: identify differentially expressed genes between clusters
### Projection of cells across dataset
* Fetch datasets in Zarr format
* K-Nearest Neighbours (KNN) mapping: The DataStore class performs KNN mapping/projection of target cells over reference cells
* Mapping scores: perform cross-dataset cluster similarity inspection
* Label transfer: transfer labels from reference cells to target cells based on majority voting
* Unified UMAPs: embed target cells onto the reference manifold
