# Variant Calling Pipeline for Whole Bacterial Genome Sequences

# Description:
<img align="center" width=500px  src="images/flowchart.jpg"></img>

# Contents:

## 1.) Data Visualization:
    - Code for parsing sample metadata from NCBI Datasets to be view with MATs in Auspice
    - Code for plotting the space complexity analysis data I found when comparing VCFs to Protobufs in this project
## 2.) paf-VCF pipeline:
    - A pipeline wrapped in snakemake and a conda environment which can be used<br>
    to perform variant calling beginning with a set of sample whole genome sequences<br>
    and a reference. For now it should be assumed that it only works with unphased <br>
    single chromosome organisms as this was made for my purposes. Also note that <br>
    variants are called in the form of only SNPs as errors occurred in the VCF merging<br>
    process when long insertions were counted. This was remedied with BCFtools norm<br>
    which I still need to do more research on. A key component to this pipeline <br>
    is the Minimap2 toolkit and paftools.js by lh3.<br>

# Application with UShER:
![alt text](/images/USA(BOLDED)vsNCTC.PNG)