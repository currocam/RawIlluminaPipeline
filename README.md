# Snakemake workflow: Raw-Illumina-Pipeline

[![Snakemake](https://img.shields.io/badge/snakemake-≥6.3.0-brightgreen.svg)](https://snakemake.github.io)
[![GitHub actions status](https://github.com/currocam/RawIlluminaPipeline/workflows/Tests/badge.svg?branch=main)](https://github.com/currocam/RawIlluminaPipeline/actions?query=branch%3Amain+workflow%3ATests)


A Snakemake workflow for raw illumine reads to draft assemblies and annotations

## Usage

First, make sure to activate the conda base environment with
``` bash
conda activate base
```

The environment.yaml file can be used to install all required software into an isolated Conda environment with the name snakemake-RawIlluminaPipeline via
``` bash
mamba env create --name snakemake-RawIlluminaPipeline --file environment.yaml
```

To activate this environment, use
``` bash
conda activate snakemake-RawIlluminaPipeline
```

To deactivate an active environment, use

``` bash
conda deactivate
```

To run the pipeline with toy data: 

```bash
snakemake results/clock_10K_prokka --cores 8
```