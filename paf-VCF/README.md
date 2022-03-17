# Snakemake Pipeline Usage:
To run, fill ```samples/``` with your input fasta sequences and ```ref/``` with reference fasta sequence. <br>
Then, make sure to install and activate the conda environment specified by ```paf2vcf.yml``` in ```envs/```.<br>
Finally, call the snakemake pipeline. <br>
<br>
For example:<br>
```$snakemake -c6 --reason --use-conda```<br>