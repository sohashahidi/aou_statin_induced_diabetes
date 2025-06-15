# Evaluating the on-target nature of statin-induced diabetes using a polygenic risk score for statin cholesterol lowering efficacy

## Overview
This repository contains data preparation and analysis code for research on the association of on-target statin LDL-lowering and statin-induced diabetes. The analysis uses personal health information (PHI), so all code and output that would reveal individual level data or summary statistics from <20 participants has been commented out and hidden. Individual level data can be viewed with controlled tier access on the National Institutes of Health's All of Us Research Program (AoURP).

## Software Used
R - Data preparation and analysis
Python - Bash scripting set-up
Bash - Job submission
Plink 2.0 - Pulling variant dosages
Regenie 4.1 - Survival genome-wide association study (GWAS)

## Notebook Descriptions
### Step 1: Data preparation
This notebook finds type 2 diabetes status, end of follow-up date, eligible statin users, and eligible statin non users.
### Step 2: Covariates
This notebook assigns covariate statuses to eligible statin users and non-users.
### Step 3: Exclusions and matching
This notebook excludes any statin users and non-users that no longer meet eligibility criteria and matches each statin user to two non-users.
### Step 4: Survival analysis
This notebook contains regression analysis (mostly survival using Cox regression, some linear regression) on multiple aspects of the data, including but not limited to: treatment group, statin intensity, change in LDL-C.
### Step 5: Genotyping
This notebook pulls candidate variants using PLINK v2.0 and runs time-to-event GWAS using Regenie v4.1.
### Step 6: Genomic analysis
This notebook contains regression analysis (mostly survival using Cox regression, some linear regression) on candidate variants and a mini polygenic score. This notebook also contains code visualizing and analyzing GWAS results.
