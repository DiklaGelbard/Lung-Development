# Lung development single cell analysis

This repository contains Rmarkdown code, R code and metadata files to build a MetaCell model and generate part of the figures for [Cohen et al. Cell 2018](www.cell.com/cell/pdf/S0092-8674(18)31181-4.pdf) Lung Single-Cell Signaling Interaction Map Reveals Basophil Role in Macrophage Imprinting, Cell 2018  

In order to run the Rmd file, downloaded processed data from the GSE119228 needs to be added in specific folders: Processed UMI-tab files (ABXXX.txt) from GSE119228 should be copied to the folder output/umi.tab.

To start analysis, run from the root directory:
R/3.5.0
library(rmarkdown)
rmarkdown::render("scripts/lung_guide.html",knit_root_dir="../")

The following R libraries should be installed:
data.table,
dplyr,
graph,
methods,
Matrix,
matrixStats,
pheatmap, 
RColorBrewer,
Rgraphviz,
KernSmooth,
zoo,
ggplot2,
cluster,
cowplot,
pdist,
doMC,
RCurl,
igraph,
RSvgDevice,
dbscan,
entropy,
parallel,
tgconfig,
tgutil (>= 0.0.3),
tgstat,
SingleCellExperiment,
BiocManager,
gridExtra,
reshape2,
scales,
metacell,
Slingshot (=3.8)


###Installation

```r
install.packages('BiocManager') 
BiocManager::install('metacell',  site_repository = 'tanaylab.bitbucket.io/repo', update = FALSE)
BiocManager::install("slingshot", version = "3.8")
```

Please send questions to [Amir Giladi](mailto:amir.goldberg@weizmann.ac.il)
