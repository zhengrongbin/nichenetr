<!-- README.md is generated from README.Rmd. Please edit that file -->
<!-- github markdown built using
rmarkdown::render("README.Rmd",output_format = "md_document")
-->

nichenetr
=========

[![Build
Status](https://travis-ci.org/saeyslab/nichenetr.svg?branch=master)](https://travis-ci.org/saeyslab/nichenetr)
[![Coverage
Status](https://codecov.io/gh/saeyslab/nichenetr/branch/master/graph/badge.svg)](https://codecov.io/gh/saeyslab/nichenetr)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.3260758.svg)](https://doi.org/10.5281/zenodo.3260758)

**nichenetr: the R implementation of the NicheNet method.** The goal of
NicheNet is to study intercellular communication from a computational
perspective. NicheNet integrates expression data of interacting cells
with prior information on potential links between ligands and target
genes. Hereby, NicheNet can be used to study how one cell (or cell type)
influences gene expression in an interacting cell (or cell type). This
type of analysis can provide novel functional insights into
intercellular signaling processes compared to limiting the analysis to
ligand-receptor inference.

Specific functionalities include:

-   assessing how well ligands expressed by a sender cell can predict
    changes in gene expression in the receiver cell
-   prioritizing ligands based on their effect on gene expression
-   inferring putative ligand-target links active in the system under
    study
-   inferring potential signaling paths between ligands and target genes
    of interest

Moreover, we provide instructions on how to make intuitive
visualizations of the main predictions.

nichenetr was tested on both Windows and Linux (R version 3.6.0)

![](vignettes/circos_plot_adapted.png)

Installation of nichenetr
-------------------------

Installation takes typically a few minutes, depending on the number of
dependencies that has already been installed on your pc. You can install
nichenetr (and required dependencies) from github with:

    # install.packages("devtools")
    devtools::install_github("saeyslab/nichenetr")

Learning to use nichenetr
-------------------------

To learn using nichenetr, read one of the following vignettes explaining
several types of analyses:

Following vignette contains the explanation on how to perform the most
basic NicheNet analysis: prioritizing ligands and predicting target
genes of prioritized ligands - this demo analysis takes only a few
minutes to run:

-   [NicheNet’s ligand activity analysis on a gene set of
    interest](vignettes/ligand_activity_geneset.md):
    `vignette("ligand_activity_geneset", package="nichenetr")`

Following vignettes contain explanation on how to do some follow-up
analyses after performing the most basic analysis:

-   [Inferring ligand-to-target signaling
    paths](vignettes/ligand_target_signaling_path.md):
    `vignette("ligand_target_signaling_path", package="nichenetr")`
-   [Assess how well top-ranked ligands can predict a gene set of
    interest](vignettes/target_prediction_evaluation_geneset.md):
    `vignette("target_prediction_evaluation_geneset", package="nichenetr")`
-   [Single-cell NicheNet’s ligand activity
    analysis](vignettes/ligand_activity_single_cell.md):
    `vignette("ligand_activity_single_cell", package="nichenetr")`
-   [Circos plot visualization to show active ligand-target links
    between interacting
    cells](vignettes/circos.md):`vignette("circos", package="nichenetr")`.

People interested in building own models or benchmark own models against
NicheNet can read one of the following vignettes:

-   [Model construction](vignettes/model_construction.md):
    `vignette("model_construction", package="nichenetr")`
-   [Model evaluation: target gene and ligand activity
    prediction](vignettes/model_evaluation.md):
    `vignette("model_evaluation", package="nichenetr")`
-   [Parameter optimization via
    mlrMBO](vignettes/parameter_optimization.md):
    `vignette("parameter_optimization", package="nichenetr")`

People working with mouse data can see in the following vignette how to
convert NicheNet’s ligand-target model (given in human symbols) to mouse
symbols:

-   [Converting NicheNet’s model from human to mouse
    symbols](vignettes/symbol_conversion.md):
    `vignette("symbol_conversion", package="nichenetr")`
