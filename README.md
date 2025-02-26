# <img src="https://github.com/user-attachments/assets/d02384b5-b85f-4716-b657-7a122ca92d02" width="100">3DisoGalaxy

This Repository contains the complete software and documentation to execute the Long-Read-translation-structomics Workflow.

## Abstract
When the alternative splicing event result in different mature mRNA translated in the cell and diverse protein isoforms produced, they tend to affect disordered protein domains, which are often involved in functionally important protein–protein interactions304,310,311. Protein isoforms can also have differences in stability, localization, enzymatic activity and protein–nucleic acid interactions. The extent to which alternative splicing affects protein and/or cell function or, rather, represents a by-product of transcriptome noise is unclear. Breast cancer is one of the most prevalent cancer for women worldwide. Current studies categorize the breast cancer into several subtypes according to different receptors and will treat with different clinical methods. The heterogeneity of the breast cancer causes this distinct survival outcome difference, and alternative splicing is one of the mechanisms of the heterogeneity. In this study, a comprehensive survey of protein isoform structures in breast cancer tissue was conducted by integrating multiple omics. 90298 was annotated and filtered by integrating long-read RNAseq transcriptome analysis and short-read RNAseq. 79815 ORFs were identified using Ribosome profiling in total. Ultimately, 46202 protein isoforms were kept and predicted structures with AlphaFold2. The "3Diso-TransFold" pipeline constructing the “3DisoGalaxy” protein structural similarity network based on multiple structure alignment scores with evaluated translated ORFs and obtained isoform structures. ORFs from the master transcriptome were retained only if identified by Ribo-seq, supporting their translation. The network reveals breast cancer and TNBC-specific isoforms, enabling subtype-specific therapeutic screening and validation. 

## Digital Object Identifiers

For the [Journal Name] Manuscript: [Paper Title]

| DOI | Description |
|-----|-------------|
| [![DOI](badge_url)](doi_link) | Contains... |
| [![DOI](badge_url)](doi_link) | Contains... |

| Categories3 Dataset | Project No.        | Type              | Sample Size | Subtypes                      | Sequencing Method               | Sequencing Platform    | Additional Information                     |
|----------------------|--------------------|-------------------|-------------|-------------------------------|----------------------------------|------------------------|--------------------------------------------|
| Assembly             | PacBio (in-house)  | BC Tissue         | 35          | Basal, Her2, LumA, LumB, NAT  | PacBio long-read mRNA-seq        | PacBio Sequel 2        | Clinical info                               |
| Discovery set        | PRJNA975550        | BC Tissue         | 86          | TNBC, Her2, LumA, LumB, NAT   | mRNA-seq                        | Illumina HiSeq 4000    | Clinical info cannot match, no RFS          |
| Microbial            | PRJNA839244        | BC Tissue         | 23          | TNBC, Her2, LumA, LumB, NAT   | mRNA-seq                        | NextSeq 550            | Clinical info, no RFS                       |
| Validation set       | PRJNA486023        | BC Tissue         | 90          | TNBC, NAT                     | mRNA-seq                        | Illumina HiSeq         | Clinical info, RFS                          |
| Fusion               | PRJNA251383        | BC Tissue         | 140         | TNBC, ER, NAT                 | mRNA-seq                        | Illumina HiSeq 2000    | Clinical information                        |
| Her2                 | PRJNA1018108       | BC Tissue         | 156         | Her2, NAT                     | mRNA-seq                        | NovaSeq 6000           | -                                           |
| Ribosome profiling   | A132 (PRJNA898352) | BC Cell line      | 24          | -                             | Ribo-seq & mRNA-seq             | Illumina HiSeq 2500    | -                                           |
| Ribosome profiling   | A133 (PRJNA523167) | BC Cell line      | 18          | -                             | Ribo-seq                        | Illumina HiSeq 4000    | -                                           |

# 3DisoGalaxy
The second pipeline, called "TranStructomics," was used to evaluate translation ORFs and predict isoform structures across transcriptome-identified transcripts, ultimately constructing a protein structural similarity network, “3DisoGalaxy,” based on multiple structure alignment scores comparing isoform structures. Specifically, the predicted ORFs from the master transcriptome were retained only if identified by Ribo-seq analysis, supporting their participation in the translation process.  
![Atlas_plan](https://github.com/user-attachments/assets/32d0ddfd-540f-49fb-aab3-fd657c5e5d14)


By combining BLASTP and HMMER methods, ORF sequences were predicted using TransDecoder and machine learning. After filtering out low-confidence and short ORFs, the longest ORF sequence was kept for each isoform, and AlphaFold-2.3 was utilized to predict protein structures. Structural similarity was then calculated using the TMalign method, collecting pairwise isoform similarities to construct a “protein universe.” Additionally, functional domains and GO term pathway annotations were assigned to the network based on UniProtKB databases.  

Through the final network, the landscape of cancer-specific alternative splicing-induced protein isoforms becomes available, allowing for the screening and validation of subtype-specific isoforms for therapeutic applications. A case study version of the final network, “3DisoGalaxy,” can be accessed at [http://hkwanglab-compbio.com:3831/](http://hkwanglab-compbio.com:3831/), and the “TranStructomics” pipeline for analyzing all data is available at [https://github.com/CityUHK-CompBio/TranStructomics](https://github.com/CityUHK-CompBio/TranStructomics).
![DOI Badge](badge_url)

We acknowledge [acknowledgement details].

We acknowledge [additional acknowledgements].

## How to use this repository and Quick Start

This workflow [brief workflow description]. To orient users [documentation overview].

### How to use this repository

This repository is organized into [organization description]. The workflow is written in [technology], allowing [benefits]. The visitor is encouraged to [contribution guidelines].

### Quick Start

This quick start and steps were performed on [system specifications].

#### Prerequisites

1. **[Software 1]**
   - Download and install from [link]
   - Configuration steps...

2. **[Software 2]**
   - Installation instructions
   - Setup details...

#### Installation Steps

```bash
# Create environment
conda create -n env_name
conda activate env_name

# Install dependencies
conda install package_name

# Clone repository
git clone https://github.com/username/repository
cd repository
```

#### Running the Pipeline

```bash
nextflow run main.nf --config config_file
```

## Documentation and Workflow

The pipeline comes with detailed documentation in the Wiki, including:

- Third-party tools
- Input parameters
- Output files
- Pipeline processes descriptions
- Vignettes:
  - [Vignette 1]
  - [Vignette 2]

## Workflow Overview
![image](https://github.com/user-attachments/assets/d0837471-63ab-4c45-a08f-7454ffe03624)

![Workflow Diagram](diagram_url)

[Workflow description]

## Using Data Resources

[Data usage description]

## Contributors

- [Name 1]
- [Name 2]
- [Name 3]

This is a joint project between [collaborating organizations].

## Citation

If you use this pipeline, please cite:

```
Citation details
```
