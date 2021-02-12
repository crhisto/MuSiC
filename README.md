Multi-subject Single Cell deconvolution (MuSiC)
=============================================

`MuSiC` is a deconvolution method that utilizes cross-subject scRNA-seq to estimate cell type proportions in bulk RNA-seq data.
![MuSiC\_pipeline](FigureMethod.jpg)

How to cite `MuSiC`
-------------------
Please cite the following publication:

> *Bulk tissue cell type deconvolution with multi-subject single-cell expression reference*<br />
> <small>X. Wang, J. Park, K. Susztak, N.R. Zhang, M. Li<br /></small>
> Nature Communications. 2019 Jan 22 [https://doi.org/10.1038/s41467-018-08023-x](https://doi.org/10.1038/s41467-018-08023-x) 

Installation
------------

``` r
# install devtools if necessary
install.packages('devtools')

# install the MuSiC package
devtools::install_github('xuranw/MuSiC')

# load
library(MuSiC)
```

More Information
-----------------
Please see [Tutorial](http://xuranw.github.io/MuSiC/articles/MuSiC.html).


Note of the current repository
---------

This repository is a fork of https://github.com/xuranw/MuSiC. It contains the following modifications: 
   - Compatibility with sparse matrices using: `dgCMatrix` objects in R.

If you want to install the MuSiC library with these modifications you can use: 

``` r
if("MuSiC" %in% rownames(installed.packages())){
  library(MuSiC)
}else{
  devtools::install_github( repo = "crhisto/MuSiC")
  library(MuSiC)
}
```

Also, you must use the following libraries with support of sparse matrix (`dgCMatrix`) for large scRNA-seq datasets: 
- Biobase: [https://github.com/crhisto/Biobase](https://github.com/crhisto/Biobase)
- xbioc: [https://github.com/crhisto/xbioc](https://github.com/crhisto/xbioc)

