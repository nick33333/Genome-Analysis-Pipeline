# Snakemake Pipeline:
## Files:
1. paf2vcf.py - Custom script by me for parsing variant call files made with paftools.js into VCF files.
2. paftools.js - Toolkit surrounding the .PAF format. Made by lh3 and found in the Minimap2 toolkit.
3. Snakefile - Snakemake pipeline script (Recommended for use with a server as a higher core count and memory will help in real time)

## Environment Setup:
Before running this pipeline, install the required conda environment using a command like: ```conda env create -f ./envs/paf2vcf.yml```

To activate the conda environment, use a command like: ```conda activate paf2vcf```

## Usage:
Use this pipeline to perform variant with whole genome assembly sequences in FASTA format. Variant call files are output in VCF format. To run, fill ```samples/``` with your input fasta sequences and ```ref/``` with reference fasta sequence. Then, make sure to install and activate the conda environment specified by ```paf2vcf.yml``` in ```envs/```. Finally, call the snakemake pipeline.


For example:<br>
```$snakemake -c6 --reason --use-conda```<br>

## Notes/Known Issues:
- Depending on the total size of the normalized VCFs produced in the last stage 
of the pipeline, the VCF merging step may fail if the computer/server you are 
working on doesn't have enough memory.
    - I've made a temporary work around where I only merge normalized VCFs in batches of
    of 500
