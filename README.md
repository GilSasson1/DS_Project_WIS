# DS_Project_WIS

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
├── Complex disorders - Data Science - 2025.pptx # David's Opening Presntation
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

