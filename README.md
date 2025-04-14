# PLINK_tutorial
This repository contains all test data and code for BBMS2003 Human Genetics PLINK course tutorial 2024-2025 Semester 2. 

PLINK version 1.9b precompiled binary can be downloaded [here](https://www.cog-genomics.org/plink/). ([32-bit or 64-bit ?](doc/system_bits.md))

# Announcements
* SNPs for LDlink can be found [here](data/ldlink_snps.txt)
* Original `pheno.txt` contained an error where FID == 0. A [fixed version](data/pheno.txt) changed FID to be the same as IID. 

# Workthrough
We assume the working directory is the directory which PLINK binary is in. If not, download PLINK from the official site above and decompress the ZIP archive. Locate the decompressed files with a file browser. Right-click the binary (plink for Mac and plink.exe for Windows), select `Get info` or `Properties`. Copy the path name and open a terminal (which you should already have by running `terminal` application [Mac] or `terminal` in the Search box [Windows]).

In the terminal prompt, type `cd` + `<SPACE>` and the path you just copied. 

Download test data `data.zip` from "Releases" on GitHub. Decompress and place all file contents in the same path as PLINK binary. 

For Windows users, replace `plink` with `plink.exe`.

**1. Converting VCF to PLINK binary formats**

``./plink --vcf alzheimers_demo.vcf.gz --make-bed --out alzheimers``

**2. Logistic modelling**

``./plink --bfile alzheimers --assoc --allow-no-sex --pheno pheno.txt --pheno-name example_pheno --out alzheimers``

**3. Result analysis and visualization**

By now, you should have generated summary statistics table of logistic association testing. You can visualize `alzheimers.assoc.logistic` using Excel or `cat` (for Mac/Linux only). Please proceed to `visualization.ipynb` and LocusZoom for additional visualization steps. 

# Contacts
Louis (snakesch@connect.hku.hk) / Leo (leiyao1997@connect.hku.hk)

