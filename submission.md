# Dataset Submission

Every dataset submission has three required components and one optional component submitted together in a data submission directory.

#### Required components:

- One **data directory** per dataset 
- One **metadata.tsv** per assay type 
- One **contributors.tsv** per dataset
    
#### Optional component, dependent upon the assay type:
- One **antibody.tsv** per dataset in which antibodies were used


If multiple datasets have been generated with the same assay_type, they may be submitted together in a single **data submission directory** with a single assay **metadata.tsv** listing all datasets, one per row (*Figure 1*). Each **data directory**  in a **data submission directory** contains the data files for a single dataset (*eg. image files, fastq files, etc*).


**![Figure 1: Example of an assay metadata.tsv]()**
*Figure 1: An assay_type-specific assay metadata.tsv lists datasets in the submission directory for that assay-type. Datasets are listed one per row. The data_path fields point to the corresponding dataset directories in the data submission directory. The contributors_path fields point to the corresponding contributors.tsv. The optional antibodies_path fields point to the corresponding antibodies.tsv.*



Figure 2 below shows the general directory structure of a data submission. Note that a **data submission directory** may contain multiple **data directories** and **metadata directories**, each directory corresponding to one dataset/row in a single assay-specific assay **metadata.tsv**.

**![Figure 2: General directory structure](TBD)**
*Figure 2: A data submission directory may contain multiple datasets for multiple assay-types. Each dataset is provided in a corresponding data directory with optional metadata provided in a corresponding metadata directory. Each assay-specific metadata.tsv (eg.codex_metadata.tsv, maldi_metadata.tsv) in the dataset submission directory lists the corresponding datasets.*


In addition, multiple assay-specific **metadata.tsvs** may be included together in a **data submission directory**. For example, the *codex-metadata.tsv* below lists datasets of the CODEX assay-type (*shown in blue*) in the submission directory while the maldi-metadata.tsv lists datasets of the MALDI assay-type (*shown in orange*) in the same **data submission directory**.


### Preparing an Assay Metadata.tsv for Data Submission

HuBMAP supports 4 categories of assays : mass spectrometry, mass spectrometry imaging, imaging and nucleotide sequence. Each assay category encompasses a variety of unique assay-types involving unique chemistries, platforms, data types and analysis tools. Below are examples of assay-types from each assay category in HuBMAP:

### mass spectrometry:
- LC-MS
- MS
- TMT

### mass spectrometry imaging:
- Imaging Mass Cytometry
- MALDI-IMS
- nanoPOTS
- nanoDESI

### imaging:
- AF
- CODEX
- multiplexed IF
- PAS microscopy
- seqFISH

### sequence:
- bulk RNA
- bulk ATAC
- scRNA-Seq
- sci-ATAC-seq
- sci-RNA-seq
- SNARE-SEQ2 (RNAseq & ATACseq)
- snATAC
- snRNA
- SPLiT-Seq
- WGS

### Assay Metadata
Data centers provide the following 4 data types (Figure 3)for each data submission to HubMAP:
**![Figure 3: Four datatypes in HuBMAP](https://lh4.googleusercontent.com/roCn5JFuGk3-tTn-n8wPL8cCOQ07t7vCZMyxuPI92LgDCIBFV4LPhKAIGgrL66b9XvuR45eeaAy9474jbfABdEoOVKam6hC0fBTshzNz0CMUaAOYhrfL3d3nsQN0VVbvV3KMMGVE)**

*Figure 3: Assay metadata, which is described in the [Assay Metadata Submission Format](https://docs.google.com/document/d/1g82GpCpFDKew60XzAO4Siaw3ZXJjwsaCpgPwhqQZxIY/edit#heading=h.qeehtnf68fas) document, is divided into 4 levels.*

### Definition of assay metadata levels

- Level 1: Are attributes that are common to all assays, for example, the type (“CODEX”) and category of assay (“imaging”), a timestamp, and the name of the person who executed the assay.
    
- Level 2: Attributes that are common to a category of HuBMAP assays, i.e. imaging, sequencing, or mass spectrometry. For example, for imaging assays this includes fields such as x resolution and y resolution.
    
- Level 3: Attributes that are specific to the type of assay, for example for CODEX that would include number of antibodies and number of cycles.
    
- Level 4: Supplementary information such a QC report or information that is unique to a lab, not required for reproducibility or is otherwise not relevant for outside groups. This information is submitted in the form of a single file, a ZIP archive containing multiple files, or a directory of files. There is no formatting requirement (although formats readable with common tools such as text editors are preferable over proprietary binary formats).

As an example, here is a link to the CODEX metadata fields, required input and descriptions: 
**[example assay metadata for CODEX](https://github.com/hubmapconsortium/ingest-validation-tools/blob/master/docs/codex/README.md)**


### How to register samples and sample data.

The [*ingest* page](https://ingest.hubmapconsortium.org) in the HuBMAP portal displays buttons to access the *HuBMAP ID* system and the *HuBMAP Data Ingest* system:

![](https://lh6.googleusercontent.com/RZYfyffyjMBI3A3CJeUl4pIj1zAhsVQvEzouYgciB3KlJAQcKz6bZAEOVi-7TC65U7kV5Eh8681DWPM9ioAPq8Ah6Fg46N5nKvU8SX_olfmvvbERbrhMPEcfF4c54D-4g--_kM-P)

- *Register or search for donors and donor samples:*
Users can register or search for donors, donor organs and tissues through the *HuBMAP ID* system. Sample data may be searched by organization that provided the donor sample, *Sample Type* and/or by keywords.
- *Register or search for assay data:*
Users can enter or search for HuBMAP data through the *HuBMAP Data Ingest* system. Data may be filtered by the organization that generated the data and/or by keywords.

### How to download data from the HuBMAP portal.

From the [*ingest* page](https://ingest.hubmapconsortium.org), search for data from *HuBMAP Data Ingest* system. Click the blue Filter button:

![](https://lh3.googleusercontent.com/qxOCLtf_W2Z-zNUgogmYy4IQOrYuHloiYgTNmsUT42J6kSfF32sFM3IxzmkPev2dgGsn8X3DvxuB7kubZ4aBlENm0yVDnOuusFU1VGEGbFzd0cKD7NfK4Irn6qFOMFZ0yrtuGrIk)

Select the **Data** link on the right side of the grid to be directed to the Globus repository. 

![](https://lh4.googleusercontent.com/g5vZzYHUGpvU8tP7bfpZYDSAMduNBZ4kP7Ug_iXbXPQoVZ0lLRSAvvC9A6nrUjmkerV2ogrMGsUjeHzLN0Pjov-gkJPdVfmGng8lq2SfaDzXtCOupLxH8zJc2_0emHJOlXlRjbBj)

The *Download* option will be listed on the right side of the the Globus directory for the selected dataset.

![](https://lh6.googleusercontent.com/o0bTXiYGmELDK6NUGZQSMcNImXGiY3JWkGzT9Nzf5qCsLzRjXSgWKsopaJZWxk-1l18eys3frlzMAZkbh4DxE6dYF10Ldov9UGTDkZZLuT25NKSvjsJd-0Tmsma29MQwK-RRInwg)


