# README
README for Acute Myeloid Leukemia Heatmap

The code provided in the README file is for generating a heatmap of gene expression data for acute myeloid leukemia (AML) samples. The heatmap is created using the pheatmap package in R. The purpose of the analysis is to cluster and visualize gene expression patterns in AML samples.

Here is a step-by-step guide to understanding and running the code:

1. Set up analysis folders:
The code creates three folders: "data", "plots", and "results".
If these folders do not exist, the code will create them using the dir.create function.
2. Import and set up data:
The code reads in two TSV files: a metadata file and a gene expression matrix file.
The metadata file contains information about the AML samples.
The gene expression matrix file contains the gene expression data for the samples.
The code uses the readr::read_tsv function to read in the TSV files.
The gene IDs are stored as row names in the gene expression matrix for further analysis.
3. Install and load libraries:
The code checks if the pheatmap package is installed and installs it if necessary using the install.packages function.
The pheatmap and magrittr libraries are loaded using the library function.
4. Choose genes of interest:
The code calculates the variance for each gene in the gene expression matrix using the var function.
It determines the upper quartile variance cutoff value using the quantile function.
It filters the gene expression matrix to select only genes with variances above the upper quartile cutoff.
5. Prepare metadata for annotation:
The code prepares the metadata for annotation by creating a new data frame.
It adds a new column to the data frame to store the mutation information for each sample.
It selects the relevant columns from the metadata file.
It sets the row names of the data frame to match the column names of the gene expression matrix.
6. Create annotated heatmap:
The code uses the pheatmap function to create a heatmap of the selected genes.
It passes the filtered gene expression matrix and the annotated metadata data frame to the pheatmap function.
The cluster_rows parameter is set to TRUE to cluster the rows (genes) in the heatmap.
The resulting heatmap object is stored in the heatmap_annotated variable.
7. Customize the appearance of the heatmap:
The code does not provide customization options for the appearance of the heatmap.
However, the pheatmap package provides various customization options, such as customizing the color palette and clustering methods.
You can refer to the documentation and examples in the provided search results for more information on customizing the heatmap appearance.