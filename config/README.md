# Introduction
This README explains how to configure the pipeline and gives several examples. 

A minimum configuration file as an example would be the following: 

```yaml
trim_galore: 
  - "--illumina" #Illumina adapter
  - "--quality 20" #Phred score
  # Don't run with `--fastqc` flag

quast:
  - "--min-contig 10" #Lower threshold for a contig length (in bp)

prokka:
  - "--prefix mygenome" #Filename output prefix [auto] (default '')
  # Don't run with `-outdir` flag 
```

The following scheme is simple: the name of the program followed by the list of program flags (as they would normally be used). 

Although not necessary, it would be ideal to: 

1. Create a custom configuration file for each use case
2. Enclose the text in quotation marks
3. Separate the different commands on different lines
4. Add comments. 

That is, although this would be perfectly valid: 

```yaml
trim_galore: 
  - --illumina --quality 20
```

This is preferable: 
```yaml
trim_galore: 
  - "--illumina" #Illumina adapter because ...
  - "--quality 20" #Phred score because ...
```
