# VCF Genotype Tools

This repository contains tools to process VCF files into genotype matrices and perform imputation on missing values, designed to handle large datasets efficiently in chunks.

## Scripts

### 1. `vcf_to_genotype_matrix.py`

Converts a VCF file into a genotype matrix with 0, 1, 2 values representing homozygous reference, heterozygous, and homozygous alternate genotypes. It reads large files in chunks and outputs a `.csv` file.

**Usage:**

```bash
python vcf_to_genotype_matrix.py
