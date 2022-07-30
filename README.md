# Scarf-workflow-PBMC
[Scarf](https://scarf.readthedocs.io/en/latest/index.html) is a Python package that performs memory-efficient analysis of single-cell genomics data. Using an efficient data chunking process (using Zarr and Dask) Scarf manages to perform the core steps of single-cell genomics data analysis with very low memory consumption. Scarf’s core step is to efficiently generate a neighbourhood graph (KNN graph) of cells.
* Format conversion: convert file into the Zarr format
* Cell filtering: 
* Feature selection: normalize data and identify the highly variable genes
* Graph creation: creating a neighbourhood graph 
* Low dimensional embedding and clustering: calculate UMAP graph
* Cell clustering: clusters identification
* Marker gene identification: identify differentially expressed genes between clusters
