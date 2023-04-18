# Single-cell DNA Methylome and 3D Multi-omic Atlas of the Adult Mouse Brain - Code and data repository

## 1. [Brain Dissection Region CCF Registration](dissection_region_ccf/)
This directory contains the CCF registration of 117 brain dissection regions, 
which can be used to quantify the anatomical composition of each dissection region,
make 3D rendering of dissection regions, select data based on spatial categories.
See README inside the directory for more details.

## 2. [Mapping Pipeline](mapping_pipeline/)
This directory contains the Snakemake mapping pipeline of snmC and snm3C cells.
See README inside the directory for more details.

## 3. [Methylome-based Clustering](clustering/)
This directory contains Jupyter notebooks for performing consensus clustering 
using chrom100k bin as features in snmC or snm3C dataset.

## 4. [Cross-modality Integration](integration/)
This directory contains Jupyter notebooks for performing cross-modality integration
between mC and RNA (using gene as features), 
mC and ATAC (using chrom5k as features) dataset.

## 5. [Merfish and RNA/mC integration](merfish)
This directory contains Jupyter notebooks for performing integration between MERFISH and RNA , MERFISH and mC (using genes as features) dataset.