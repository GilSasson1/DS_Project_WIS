# DS_Project_WIS

## Overview 
1. We made an excel spreadsheet named "Human specific diseases.xlsx" containing information for all the diseases we curated.
2. We decided which cell types play a role in each disease (sources in the deep search directory).
3. Used the full GWAS catalog to filter the relevent diseases and made a spreadsheet containing information on associated genes, effect sizes and number of nornalized studies the genes are mentioned in (gwas.ipynb -> traits.xlsx).
4. We merged the the selcted GWAS genes with Clinvar genes for each disease (merge_genes.ipynb -> joint_gene_list_per_trait.pkl)
5. Conducted Fisher's Exact test between a list of associated to disease genes (gwas_mapped & clinvar) and all the other genes (**all the mapped genes from gwas that are associated to a human specific disease** + all of the other genes in the full clinvar catalog) for ASE and NonASE, and inside the ASE group between upregulated and down regulated genes. Creating all of the plots in the specified directories (ASE_analysis_organized.ipynb -> all the figures dirs + fisher_for_all_data.xlsx).
6. In the ASE analysis we conducted fisher's test for different percentiles of LFC (absloute value & not). Hence, we took genes from every group and conducted the test between them and all the background genes (ase/nonase + up/down regulation)
and we calculted the spearman correlation bettween the effect sizes of all the tests. This was only for Schizophernia and Scoliosis. (i.e. ASE_analysis_organized.ipynb -> correlation_regulation_LFC_bins)
7. 

## Repository Structure

 ```
DS_Project_WIS/
├── .gitignore
├── ASE_analysis_organized.ipynb #  Main Analysis notebook
├── gwas.ipynb # GWAS preprocessing and analysis
├── merge_genes.ipynb # Merging gene lists across traits and catalogs
├── ASE_info.tsv # Raw ASE metadata
├── traits.xlsx # Output sheet of gwas.ipynb
├── fisher_for_all_data.xlsx # Fisher’s exact test results
├── joint_gene_list_per_trait.csv/.pkl # Gene lists per trait from Clinvar and GWAS (output file of merge_genes.ipynb)
├── correlation_*.csv # Schizophernia Correlation tables 
├── *.png / *.pdf # Figures (effect sizes, distributions, etc.)
├── LFC_histograms/ # Histograms of LFC for all cell types and diseases
├── ase_genes_pie_charts/ # Pie‑chart notebooks & outputs
├── deep search # Outputs LLM deep research on celltypes associated to diseases
├── … # (other visualization folders)
├── Complex disorders - Data Science - 2025.pptx # David's Opening Presentation
└── final_presentation.pptx # Our Presentation
 ```


### Data
 ```
ASE_info.tsv — allele‑specific expression metadata
traits.xlsx — list of traits & mappings
fisher_for_all_data.xlsx — Fisher’s exact test summaries
Human specific diseases: An excel spreadsheet summarizing human specific diseases info
 ```

### Notebooks
 ```
File |	Purpose
ASE_analysis_organized.ipynb |	Full ASE workflow: Running this notebook outputs most of the figures (Stacked barplots, grouped stacked barplots, correlations for schizophrenia, regulations distributions, etc...) 
gwas.ipynb |	GWAS summary stats, effect‑size distributions
merge_genes.ipynb |	Combine Clinvar & GWAS gene lists across traits
 ```

### Figures & Outputs
 ```
LFC_histograms: LFC histograms for all cell types
ase_genes_pie_charts: Pie charts of ase/nonase/else
barplots_with_else: Stacked barplots for fisher's for all genes
barplots_post_filtration_no_else: Stacked barplots for ase/nonase only
barplots_ASE_with_regulation_direction: Stacked barplots for up/down regulation (ASE) only
lfc_or_plots_per_threshold: Spearman correlation between bins of fisher's tests for all celltypes and diseases
schizophernia_correlations: Spearman Correlations for Schizophernia cells only + densities of ASE types + manwhitney test between low and high count groups
scoliosis_correlations: Spearman Correlations for scoliosis only + densities of ASE types.
 ```

