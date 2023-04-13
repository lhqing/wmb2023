# snmC-seq3 and snm3C-seq Mapping Pipeline

## Installation
To install mapping packages, we recommend using python package manager mamba (faster) or conda:
- mamba: https://mamba.readthedocs.io/en/latest/
- conda/miniconda: https://docs.conda.io/en/latest/miniconda.html

All the packages and mapping environment can be created by 
```
# this creates a environment called mapping, containing all packages
mamba env create -f mapping_env.yaml
# activate the enviroment before run mapping
mamba activate mapping
```

## Build genome index
Bismark genome index is built by `bismark_genome_preparation` using default parameters, see documentation in:
https://rawgit.com/FelixKrueger/Bismark/master/Docs/Bismark_User_Guide.html

All genome sequence and related files downloaded from:
https://hgdownload.cse.ucsc.edu/goldenpath/mm10/bigZips/

## Run mapping

```
# run snmC mapping
cd snmC_example/
snakemake -j n_cpu --snakefile ./Snakefile

# run snm3C mapping
cd snm3C_example
snakemake -j n_cpu --snakefile ./Snakefile

```

## Mapping steps for a single cell
### snmC
![snmc](https://raw.githubusercontent.com/lhqing/wmb2023/main/mapping_pipeline/snmC_example/snmC_steps.svg)
### snm3C
![snm3c](https://raw.githubusercontent.com/lhqing/wmb2023/main/mapping_pipeline/snm3C_example/snm3C_steps.svg)


## Mapping example files:
```
.
├── mapping_env.yaml  # package information YAML file, can be used by mamba/conda to create mapping environment
├── snm3C_example  # minimum snm3C Bismark mapping pipeline example
│   ├── Snakefile
│   ├── fastq
│   │   ├── CEMBA3C_18A3C_R2_P10-1-O5-A2-R1.fq.gz
│   │   └── CEMBA3C_18A3C_R2_P10-1-O5-A2-R2.fq.gz
│   ├── mm10.main.chrom.sizes
│   └── snm3C_steps.svg  # visualization of snm3C mapping steps
└── snmC_example  # minimum snmC Bismark mapping pipeline example
    ├── Snakefile
    ├── fastq
    │   ├── CEMBA200707_9E_1-1-A18-A1-R1.fq.gz
    │   └── CEMBA200707_9E_1-1-A18-A1-R2.fq.gz
    └── snmC_steps.svg  # visualization of snmC mapping steps
```
