# Repository to explore various types of spatial transcriptomics and proteomics datasets 

## Types of spatial data being generated 

### Spatial image-based and sequencing-based transcriptomics methods

- insta-seq: https://www.biorxiv.org/content/10.1101/722819v1
- bar-seq: https://www.biorxiv.org/content/10.1101/294637v2

### Spatial proteomics 

- 4i: https://www.ncbi.nlm.nih.gov/pubmed/30072512
- cycif: https://www.cycif.org/
- codex: https://www.akoyabio.com/application/files/7015/6625/6771/CODEX_Brochure_Aug_2019_WEB.pdf


## Spatial data infrastructure 

There are various types of proposed spatial data infrastructure to store and analyze spatial data in R/Bioconductor or Python:

- `starfish` schema ([docs available here](https://spacetx-starfish.readthedocs.io/en/latest/getting_started/index.html))) 
    - Pros: has a schema for a spatially-localized gene expression matrix that supports with transcriptomics and proteomics and spatial sequencing methods
    - Cons: 
- `Giotto` data structure ([R package available](http://spatial.rc.fas.harvard.edu/giotto-viewer/))
    - Pros: 
    - Cons: 
- `Spaniel` data infrastructure ([Bioconductor package available](https://bioconductor.org/packages/release/bioc/html/Spaniel.html)) -- stores the processed data (count matrix) from spatial transcriptomics in a `SingleCellExperiment` object, with x/y coordinates in the `colData`. The image is then read in separately.
    - Pros: 
    - Cons: (1) might be better to define a slot rather than storing as metadata (to enable validity checks) and (2) like `SingleCellExperiment`, make a package dedicated to the data structure, and leaving plotting functions to downstream packages
- `SpatialCellExperiment` package ([available on GitHub](https://github.com/kevinrue/SpatialCellExperiment)). 
    - Pros: 
    - Cons: 
- https://akoyabio.github.io/phenoptr/


## Datasets

### Analysis of 10x Visium mouse brain tissue (strain C57BL/6)

This [Visium data](https://support.10xgenomics.com/spatial-gene-expression/datasets/1.0.0/V1_Adult_Mouse_Brain) come from the 10x website and there is a short description provided: 

> "10x Genomics obtained fresh frozen mouse brain tissue (Strain C57BL/6)from BioIVT Asterand. The tissue was embedded and cryosectioned as described in Visium Spatial Protocols - Tissue Preparation Guide (Demonstrated Protocol CG000240). Tissue sections of 10 µm thickness from a slice of the coronal plane were placed on Visium Gene Expression Slides."

Code and analysis available [here](data-analyses/visium-mouse-brain-strain-C57BL6.Rmd).


## Useful resources

- [presentation from Lars Borm (Linnarsson lab)](https://nbisweden.github.io/single-cell_sib_scilifelab/session-outlook/Spatial_Lars-Borm_NBIS2019.pdf)
- [lit review by Ambrose](https://docs.google.com/spreadsheets/d/1tLTJrGul6p_4dpiT1_uU46HFCj-EE2mABXwSxqfCryQ/edit?usp=sharing) 
- [slides from Ruben Dries on `giotto`](https://www.dropbox.com/s/4e0a9qrk8zhm900/191106_meetup_spatial_transcriptomics_small.pdf?dl=0)


# Contributors

- Stephanie C. Hicks [[@stephaniehicks](https://github.com/stephaniehicks/)]
