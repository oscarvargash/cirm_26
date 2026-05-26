# Day 3

## Runing a Seurat tutorial

1. Please log into your lab computer and create a working directory `day_3`. Alternatively you can login into https://vlab.humboldt.edu if working remotely.

2. Download the following data https://cf.10xgenomics.com/samples/cell/pbmc3k/pbmc3k_filtered_gene_bc_matrices.tar.gz and place it in `Documents`

3. This is a compressed file. Double-click on the cpmressed file and copy the folder `filtered_gene_bc_matrices` into the `day_3` folder created previously. Our working directory will be the folder `hg19`, which is nested in `filtered_gene_bc_matrices`

4. Set the folder `hg19` as your working directory (in RStudio > Session > set working directory)

```
setwd("YOUR_USER/Documents/day_3/sfiltered_gene_bc_matrices/hg19/")
```

5. Install the following packages

***NOTE*** when the Rstudio asks "Do you want to install from sources the package which needs compilation?" answer "NO"

```
install.packages("dplyr")
install.packages("Seurat")
install.packages("patchwork")


library(dplyr)
library(Seurat)
library(patchwork)
```

6. Import the data

```
pbmc.data <- Read10X(data.dir = ".")
```


7. Follow the tutorial found here https://satijalab.org/seurat/articles/pbmc3k_tutorial.html  

