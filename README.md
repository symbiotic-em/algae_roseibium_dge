# DGE, GO MWU and Growth Stats Analysis for Long-Term Cocultures of Symbiodiniaceae-Roseibium 
Accompanying script and input/output files to the manuscript in preparation:
"Symbiodinium-Roseibium establish a stable coculture and exhibit synergistic growth effects" by Emily G Aguirre, et.al

Here, we grew axenic cultures of S. linucheae (strain SSA01) and Roseibium in B12-limited media for 12 weeks, followed by differential gene expression analysis comparing controls (axenic SSA01 or axenic Roseibium) and coculture treatments. 

All analyses can be re-created by starting with the raw .fastq files available upon request to EG Aguirre (emilyagu@usc.edu or aguirre.emilyg@gmail.com) or CD Kenkel (ckenkel@usc.edu)
A full annotation of the Roseibium sp. Sym1 genome can be found at JGI IMG/MER under Project ID: Gp0612333, under "Roseibium sp. Sym1 re-assembly" (https://gold.jgi.doe.gov/projects?id=Gp0612333).

# Files in this repository 

Raw reads QC to counts
- roseibium_raw_reads_to_counts_script      Roseibium pipeline
- SSA01_raw_reads_to_counts_script     SSA01 pipeline


DESeq2 analysis for Roseibium
- DESeq2_bacteria_script      DESeq2 bacterial analysis
- curated_final_bac_tpm.tab     Roseibium concatenated counts by TPM, as generated by salmon
- 0521_bac_deseq2_by_type_res.csv     DESEq2 results by ~Type


DESeq2 analysis for SSA01
- DESeq2_SSA01_script     DESeq2 SSA01 analysis
- algae_counts2.tab     SSA01 concatenated counts by TPM as generated by salmon
- model_algae_type_res.csv    DESeq2 results by ~Type
- model_algae_type_plus_treatment_res.csv     DESeq2 results by ~Type+treatment


GO MWU analysis
- GO_MWU_analysis_CKenkel_version     GO MWU analysis script
- rose_gene.tab     input file
- rose_go.tab     input file
- ssa01_gene.tab    input file
- ssa01_final_go.tab      input file


Growth stats for Roseibium 
- rose_growth_stats_script    Roseibium stats script
- SSA01_growth_stats_script     SSA01 stats script
- b12_roseibium_for_lm.csv    input file for plotting a graph for Roseibium
- b12_starved_vs_b12coculture_counts.csv    input file for ANOVA for Roseibium
- posthoc_rose_mono_vs_coculture_stats.csv    statistical output 

Growth stats for SSA01
- b12_counts_for_lm_ck.csv     input file for plotting a graph for SSA01 and Welch t-test
- ssa01_counts_for_anova.csv    input file for ANOVA for SSA01
- posthoc_ssa01_all_treatments_stats.csv    statistical output, two-way repeated measures ANOVA, posthoc t-test
- Round 1, Round 2, Round 3 folders     folders containing input files for three subculturing, no B12 trials of SSA01 and post-hoc t-tests statistical output
- t-tests_time.csv    statistical output for Welch t-test in raw dataframe
- t-tests_pvalues_padj.csv    cleaned statistical output (t-tests_time.csv) and formatted for addition of p.adjusted value
- compat_adj.pvalues.csv    same dataframe as above (t-tests_pvalues_padj.csv), but with p.adjusted values


BLAST results of SSA01 transcriptome blasted to metE/metH sequences from Lin et al. (2022) found at --> https://doi.org/10.1016/j.fmre.2021.12.014
- metE_metH_SSA01_BLAST_results  



