# VCF Genotype Tools

This repository provides tools for processing large VCF (Variant Call Format) files into genotype matrices and imputing missing values. The pipeline is designed to efficiently handle large genomic datasets in **chunks**, minimizing memory usage.

## 🧬 Overview

The pipeline consists of **two main steps**:

1. **Convert a VCF file to a genotype matrix**
2. **Impute missing values (non-PAVs)**

---

## 🧩 Step 1: VCF to Genotype Matrix (`vcf_to_genotype_matrix.py`)

This script processes a VCF file and converts it into a matrix of genotypes encoded as:

- `0` = Homozygous Reference (`0/0`)
- `1` = Heterozygous (`0/1`)
- `2` = Homozygous Alternate (`1/1`)
- `NaN` = Missing/Other values

The script reads the VCF in **chunks** for memory efficiency and outputs a `.csv` file.

### 🔧 Example usage:

```bash
python vcf_to_genotype_matrix.py
