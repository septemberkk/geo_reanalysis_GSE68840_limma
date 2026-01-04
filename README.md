# geo_reanalysis_GSE68840_limma

# GSE68840 reanalysis (GPL13938-11302) —  (limma)

This is a reanalysis of **GSE68840** (Illumina HumanHT-12 WG-DASL V4.0, GPL13938-11302).

## Dataset
- GEO: GSE68840  
- Platform: GPL13938-11302
- Data type: Expression profiling by array (microarray)
- Biological contrast: **Resistant vs Parental** 


## Methods (summary)
- Differential expression: **limma**
- Significance threshold:
  - `adj.P.Val < 0.05`
  - `|logFC| > log2(1.5)` (≈ 0.585)

## Files
### Input
- `GSE68840_Matrix.txt`  
  Probe-level expression matrix (rows = probes, columns = samples).
- `GPL13938-11302.txt`  
  Probe annotation table used to map probes to `GENE_SYMBOL`.

### Script
- `scripts/run_limma_GSE68840.R`  

### Output
- `results/all_DEG.txt`  
  Full limma table + gene symbol.
- `results/sig_DEG.txt`  
  Filtered DEGs with the thresholds above.
- `results/RNA_expression_boxplot.pdf`  
  Per-sample distribution check.
- `results/RNA_expression_MDS.pdf`  
  Sample separation (limma `plotMDS`).
- `results/DEG_volcano.pdf`  
  Volcano plot.

## How to run
In R:

```r
source("scripts/run_limma_GSE68840.R")
