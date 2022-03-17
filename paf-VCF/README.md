# Snakemake Pipeline:
## Files:
1. paf2vcf.py - Custom script by me for parsing variant call files made with paftools.js into VCF files.
2. paftools.js - Toolkit surrounding the .PAF format. Made by lh3 and found in the Minimap2 toolkit.
3. Snakefile - Snakemake pipeline script (Recommended for use with a server as a higher core count will help in real time)

## Usage:
To run, fill ```samples/``` with your input fasta sequences and ```ref/``` with reference fasta sequence. <br>
Then, make sure to install and activate the conda environment specified by ```paf2vcf.yml``` in ```envs/```.<br>
Finally, call the snakemake pipeline. <br>
<br>
For example:<br>
```$snakemake -c6 --reason --use-conda```<br>