# DEA
differential expression analysis
# Transcriptomics Analysis

This repository contains R scripts and workflows used in the differential expression and mitochondrial gene analysis of brain-derived transcriptomic data from ALS patient and control samples. The project specifically focuses on nuclear-encoded mitochondrial (NEM) genes using DESeq2, MitoCarta3.0, and functional enrichment analyses.

---

## 📁 Project Structure

├── scripts/ # All R scripts for data processing and analysis
├── data/ # (not included) Expected input files (see below)
├── results/ # Processed output and summary tables
├── figures/ # Volcano plots, Venn diagrams, etc.
└── README.md # This file

---

## ⚙️ Requirements

- R version >= 4.4.2
- Packages:
  - DESeq2
  - biomaRt
  - org.Hs.eg.db
  - ggplot2
  - VennDiagram
  - dplyr
  - clusterProfiler
  - (and others — listed in `renv.lock` or `requirements.R`)

You can install required packages using:

```r
install.packages("BiocManager")
BiocManager::install(c("DESeq2", "biomaRt", "org.Hs.eg.db"))
```
---

## 📂 Data Availability

The original transcriptomic data used in this analysis are not included in this repository due to privacy restrictions. The pipeline expects input files such as:

counts_nmtRNA_TALS.csv – filtered raw counts for TALS dataset
coldata_nmtRNA_TALS.csv – metadata (sex, age, RIN, diagnosis, etc.)

---

## 🚀 How to Run

This project is contained in a single R Markdown file:

- `DEG_nmtRNA_TALS.Rmd`

### 📥 To Run:

1. Open the file in **RStudio**
2. Make sure your expected data files are present in the `data/` folder (e.g., `counts.csv`, `coldata.csv`)
3. Click the **Knit** button in RStudio (top bar), or run:

```r
rmarkdown::render("DEG_nmtRNA_TALS.Rmd")
```

📊 Outputs

Volcano plots highlighting significant NEM DEGs
Annotated tables of DEGs with HGNC and ENTREZ IDs
KEGG and GO enrichment 

---

🔒 License

This repository is for academic/research purposes. Contact the author for licensing or collaboration inquiries.

---

📧 Contact

For questions or collaboration:
Name: [Shahad]
Email: [sh.lens333@gmail.com]



