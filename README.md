
# Sex-Chromosome Dosage Analysis in the Horse (*Equus caballus*)

## Student Information

- **Name:** Klea Mae G. Estrellanes
- **Student Number:** 202400728
- **Course:** BS Biology – Cell and Molecular Biology
- **Section:** B
- **Selected Organism:** *Equus caballus* (Horse)
- **Analysis:** X-Chromosome Dosage Estimation Using Whole-Genome Sequencing Read Depth

---

## 1. Project Overview

This project investigates whether whole-genome sequencing (WGS) read-depth analysis can be used to estimate X-chromosome dosage in the horse (*Equus caballus*).

The analysis uses the chromosome-level reference assembly EquCab3.0 and paired-end WGS reads obtained from the NCBI Sequence Read Archive (SRA). The sequencing reads were processed and aligned using Galaxy. Chromosome-specific coverage was calculated using Samtools Coverage, and the resulting data were analyzed using a base-R script.

The X-chromosome mean sequencing depth was compared with the median sequencing depth of the autosomes to calculate the X-to-autosome ratio (X:A).

The analysis produced an **XX-like dosage inference**. This result is consistent with the female sex reported in the WGS BioSample metadata. However, read-depth analysis is an indirect genomic method and does not constitute definitive karyotyping.

## 2. Study Question

Can whole-genome sequencing read depth mapped to the EquCab3.0 reference assembly be used to estimate X-chromosome dosage in *Equus caballus*?

The study evaluates chromosome-specific sequencing depth by comparing the X chromosome with the median depth of the autosomes.

The expected X:A ratios under a conventional diploid XX/XY system are approximately:

- **XX complement:** X:A ratio near 1.0
- **XY complement:** X:A ratio near 0.5

These expected values provide a biological basis for interpreting relative chromosome dosage.

## 3. Selected Species and Sex-Chromosome System

- **Scientific name:** *Equus caballus*
- **Common name:** Horse
- **Sex-chromosome system:** XX/XY
- **Reference assembly:** EquCab3.0
- **Assembly accession:** GCF_002863925.1
- **Assembly level:** Chromosome

The horse has a conventional mammalian XX/XY sex-determination system. Females typically possess two X chromosomes (XX), whereas males typically possess one X chromosome and one Y chromosome (XY).

The selected reference assembly contains 31 autosomes and an annotated X chromosome. The chromosome identities were verified using the NCBI assembly report.

**Important assembly limitation:** The selected EquCab3.0 reference assembly does not contain an annotated Y chromosome in its primary chromosome-level sequence records. Therefore, a Y-to-autosome depth ratio could not be calculated from this reference.

## 4. NCBI Accession Information

### 4.1 Reference Genome Assembly

| Information | Accession or description |
|---|---|
| Organism | *Equus caballus* |
| Assembly name | EquCab3.0 |
| RefSeq assembly accession | GCF_002863925.1 |
| GenBank assembly accession | GCA_002863925.1 |
| Assembly BioSample | SAMN02953672 |
| Assembly donor/isolate | Twilight |
| Reported assembly donor sex | Female |
| Assembly level | Chromosome |

The assembly report identifies the reference donor as the Thoroughbred isolate Twilight and records the donor sex as female.

**NCBI resources:**

- [NCBI Assembly – GCF_002863925.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCF_002863925.1/)
- [NCBI BioSample – SAMN02953672](https://www.ncbi.nlm.nih.gov/biosample/SAMN02953672)

### 4.2 Whole-Genome Sequencing Dataset

| Information | Accession or description |
|---|---|
| Organism | *Equus caballus* |
| WGS run | SRR25750664 |
| Experiment | SRX21474078 |
| WGS BioSample | SAMN37129746 |
| BioProject | PRJNA1005486 |
| Sample name | WB03 |
| Tissue | Blood |
| Reported WGS donor sex | Female |
| Library strategy | Whole-genome sequencing (WGS) |
| Sequencing platform | Illumina NovaSeq 6000 |
| Library layout | Paired-end |
| Read length | 150 bp |

The paired-end reads used in Galaxy were:

```text
SRR25750664:forward
SRR25750664:reverse
```

**NCBI resources:**

- [NCBI SRA – SRR25750664](https://www.ncbi.nlm.nih.gov/sra/SRR25750664)
- [NCBI BioSample – SAMN37129746](https://www.ncbi.nlm.nih.gov/biosample/SAMN37129746)
- [NCBI BioProject – PRJNA1005486](https://www.ncbi.nlm.nih.gov/bioproject/PRJNA1005486)

### 4.3 Assembly Donor and WGS Donor Comparison

The assembly BioSample and WGS BioSample are different records:

- Assembly donor: SAMN02953672
- WGS donor: SAMN37129746

The two BioSample accessions do not establish that the samples came from the same individual. Therefore, the assembly donor and WGS donor are treated as **different individuals for this analysis**.

Both BioSample records report female sex. The XX-like read-depth result is compared with the sex metadata of the WGS donor, not automatically attributed to the assembly donor.

## 5. Reference Genome and Chromosome Identification

The reference genome used in this analysis was:

```text
GCF_002863925.1_EquCab3.0_genomic.fna.gz
```

The corresponding NCBI assembly report was:

```text
GCF_002863925.1_EquCab3.0_assembly_report.txt
```

The assembly report was used to identify the chromosome accessions and distinguish assembled chromosomes from unplaced scaffolds and non-nuclear sequences.

### 5.1 Autosomes

The following 31 RefSeq accessions represent the horse autosomes:

| Chromosome | RefSeq accession | Group |
|---|---|---|
| 1 | NC_009144.3 | A |
| 2 | NC_009145.3 | A |
| 3 | NC_009146.3 | A |
| 4 | NC_009147.3 | A |
| 5 | NC_009148.3 | A |
| 6 | NC_009149.3 | A |
| 7 | NC_009150.3 | A |
| 8 | NC_009151.3 | A |
| 9 | NC_009152.3 | A |
| 10 | NC_009153.3 | A |
| 11 | NC_009154.3 | A |
| 12 | NC_009155.3 | A |
| 13 | NC_009156.3 | A |
| 14 | NC_009157.3 | A |
| 15 | NC_009158.3 | A |
| 16 | NC_009159.3 | A |
| 17 | NC_009160.3 | A |
| 18 | NC_009161.3 | A |
| 19 | NC_009162.3 | A |
| 20 | NC_009163.3 | A |
| 21 | NC_009164.3 | A |
| 22 | NC_009165.3 | A |
| 23 | NC_009166.3 | A |
| 24 | NC_009167.3 | A |
| 25 | NC_009168.3 | A |
| 26 | NC_009169.3 | A |
| 27 | NC_009170.3 | A |
| 28 | NC_009171.3 | A |
| 29 | NC_009172.3 | A |
| 30 | NC_009173.3 | A |
| 31 | NC_009174.3 | A |

### 5.2 X Chromosome

| Chromosome | RefSeq accession | Group |
|---|---|---|
| X | NC_009175.3 | X |

The X chromosome was identified from the NCBI assembly report, which lists it as an assembled chromosome.

### 5.3 Excluded Sequences

The following sequence categories were not classified as autosomes:

- Mitochondrial DNA
- Unplaced scaffolds
- Alternate haplotypes
- Other non-autosomal sequences

The mitochondrial accession NC_001640.1 was excluded from the chromosome grouping.

The selected reference did not provide an annotated Y chromosome among its primary assembled chromosome records. Consequently, no Y chromosome was included in the chromosome grouping file.

## 6. Galaxy Analysis

### 6.1 Galaxy History

The sequencing analysis was conducted using Galaxy.

- **History name:** `Sex_Dosage_Horse`
- **Galaxy history link:** [Open Galaxy History](https://usegalaxy.org/u/estrellanes_08/h/sex-dosage-horse)

The reference genome and WGS reads were imported into the same Galaxy history.

### 6.2 Reference Genome Import

The EquCab3.0 genomic FASTA file was imported into Galaxy.

```text
GCF_002863925.1_EquCab3.0_genomic.fna.gz
```

This reference was used as the genomic coordinate system for subsequent read alignment.

### 6.3 WGS Read Import

The WGS run SRR25750664 was imported using the Galaxy SRA FASTQ import tool.

The resulting paired-end datasets were:

```text
Dataset 7: SRR25750664:forward
Dataset 8: SRR25750664:reverse
```

The two read files were retained as paired-end sequencing data for alignment.

### 6.4 Read Quality Assessment

FastQC was used to evaluate the quality characteristics of the sequencing reads before alignment. MultiQC was used to summarize the quality-control reports.

The quality-control assessment included:

- Per-base sequence quality
- Per-sequence quality scores
- Per-sequence GC content
- Sequence length distribution
- Adapter content
- Sequence duplication levels
- General read-quality indicators

The MultiQC summary showed:

| Metric | Forward reads | Reverse reads |
|---|---:|---:|
| Total sequences | 92,313,702 | 92,313,702 |
| Mean sequence length | 150 bp | 150 bp |
| Median sequence length | 150 bp | 150 bp |
| GC content | 42% | 42% |
| Duplicate reads | 16.49% | 15.69% |
| FastQC failed modules | 0 | 0 |

The absence of failed FastQC modules indicates that no module was classified as failed in the reported FastQC summary. It does not mean that every sequencing-quality characteristic was perfect.

The duplication percentages represent reads identified as duplicates by the quality-control assessment. They should not be confused with the duplicate count reported by a separate alignment statistic.

### 6.5 Read Alignment Using BWA-MEM2

The paired-end WGS reads were aligned to the EquCab3.0 reference genome using **BWA-MEM2**.

The actual Galaxy job configuration was verified from the job details.

| Parameter | Actual configuration |
|---|---|
| Reference genome | Dataset 2 |
| Reference file | GCF_002863925.1_EquCab3.0_genomic.fna.gz |
| First read set | Dataset 7 – SRR25750664:forward |
| Second read set | Dataset 8 – SRR25750664:reverse |
| Read configuration | Paired-end |
| BAM sorting mode | Sort by chromosomal coordinates |
| Output | Dataset 29 – BAM |
| Job state | OK |
| Tool exit code | 0 |

The alignment produced:

```text
Dataset 29:
BWA-MEM2 on dataset 2, 7, and 8
(mapped reads in BAM format)
```

The BAM output was coordinate-sorted according to the BWA-MEM2 job parameters.

A separate BAM index dataset was not found in the Galaxy history. Therefore, this report does not claim that a separate `.bai` file was generated.

### 6.6 Alignment Statistics

Samtools Flagstat was used to summarize the alignment output.

The reported statistics were:

| Alignment metric | Result |
|---|---:|
| Total reads | 184,965,240 |
| Primary reads | 184,627,404 |
| Mapped reads | 184,670,143 |
| Mapping rate | 99.84% |
| Properly paired reads | 181,356,252 |
| Properly paired percentage | 98.23% |
| Singletons | 136,543 |
| Singleton percentage | 0.07% |
| Marked duplicates | 0 |

The high mapping percentage indicates that most reads were aligned to the selected reference under the alignment tool's reported statistics.

The zero duplicate count in Flagstat means that no reads were marked as duplicates in that BAM. It does not establish that the original sequencing library contained no PCR or optical duplicates.

### 6.7 Samtools Coverage

Chromosome-specific sequencing depth was calculated using Galaxy's **Samtools Coverage** tool.

The tool was run using Dataset 29 as the BAM input.

The actual job parameters were verified from the Galaxy dataset details:

| Parameter | Actual setting |
|---|---|
| BAM input | Dataset 29 – BWA-MEM2 BAM |
| Pooling BAM files | False |
| Minimum read length | 0 |
| Minimum mapping quality | 20 |
| Minimum base quality | 20 |
| Histogram | False |
| Output | Dataset 33 – Samtools Coverage |
| Job state | OK |
| Tool exit code | 0 |

The BAM files were not pooled. The coverage calculation was performed on the individual WGS dataset.

The minimum mapping quality and minimum base quality were both set to 20 to reduce the contribution of low-confidence alignments and low-quality bases.

The resulting tabular output was downloaded and saved as:

```text
chromosome_coverage.tsv
```

The coverage table contained the required fields:

```text
rname
meandepth
```

The file contained 4,701 lines and 9 columns.

The `rname` field identifies each reference sequence, while `meandepth` represents the mean sequencing depth calculated for that sequence.

### 6.8 Galaxy Dataset Summary

| Dataset | Description |
|---|---|
| 2 | EquCab3.0 reference genomic FASTA |
| 7 | Forward WGS reads |
| 8 | Reverse WGS reads |
| 21 | FastQC Webpage |
| 22 | FastQC RawData |
| 27 | MultiQC Webpage |
| 28 | MultiQC statistics table |
| 29 | BWA-MEM2 coordinate-sorted BAM |
| 30 | Samtools Flagstat |
| 31 | Mosdepth depth distribution |
| 32 | Mosdepth summary |
| 33 | Samtools Coverage tabular output |

Mosdepth outputs were retained as supplementary coverage summaries. The chromosome-depth analysis described in this report used the Samtools Coverage output.

## 7. Chromosome Grouping File

A CSV file named:

```text
chromosome_groups.csv
```

was prepared for the R analysis.

The first line of the file was:

```csv
rname,group
```

The file contained the 31 autosomes and one X chromosome, using the exact RefSeq sequence identifiers.

The grouping was:

- `NC_009144.3` through `NC_009174.3` — autosomes (A)
- `NC_009175.3` — X chromosome (X)

The mitochondrial genome and unplaced scaffolds were excluded.

The chromosome identifiers were obtained from the NCBI assembly report and matched against the reference sequence names used in the coverage analysis.

## 8. R Analysis

The chromosome-depth analysis was performed using RStudio and the base R programming language.

No additional R packages were required.

The analysis used the following input files:

```text
chromosome_coverage.tsv
chromosome_groups.csv
```

The R script was saved as:

```text
sex_depth_analysis.R
```

### 8.1 Analytical Procedure

The script performed the following operations:

1. Imported the Samtools Coverage tabular output.
2. Standardized the first column name to `rname`.
3. Imported the chromosome grouping CSV file.
4. Matched chromosome identifiers between the two input files.
5. Converted mean-depth values to numeric data.
6. Checked for missing or invalid depth values.
7. Calculated the median autosomal sequencing depth.
8. Calculated chromosome-relative depth.
9. Calculated the X:A ratio.
10. Applied the classroom interpretation thresholds.
11. Generated a chromosome-depth plot.
12. Exported the relative-depth table and sex-inference summary.

### 8.2 Interpretation Thresholds

The laboratory script uses the following classroom interpretation guidelines:

| X:A ratio | Interpretation |
|---|---|
| ≥ 0.80 | XX-like |
| ≤ 0.65 | XY-like |
| Between 0.65 and 0.80 | Ambiguous |

These are instructional thresholds for the practical exercise. They are not validated clinical or diagnostic cutoffs.

### 8.3 Generated R Outputs

The analysis generated the following files:

```text
results/
├── chromosome_relative_depth.csv
├── chromosome_depth.png
└── sex_inference.txt
```

The outputs contain the normalized chromosome-depth measurements, the graphical representation of relative depth, and the summary of the dosage inference.

## 9. Results

### 9.1 Median Autosomal Sequencing Depth

**9.673×**

The median autosomal depth was calculated from the mean-depth values of the 31 autosomes.

The median was used as the normalization reference to reduce the influence of unusually high or low chromosome-specific coverage values.

### 9.2 X-Chromosome Dosage

**X:A ratio: 0.974**

The X:A ratio was calculated by dividing the mean sequencing depth of the X chromosome by the median sequencing depth of the autosomes.

\[
X:A = \frac{\text{Mean X-chromosome depth}}
{\text{Median autosomal depth}}
\]

The resulting ratio of 0.974 is close to the expected value of approximately 1.0 for an XX complement.

### 9.3 Y-Chromosome Dosage

**Y:A ratio: NA**

The selected EquCab3.0 reference assembly does not contain an annotated Y chromosome in its primary chromosome-level sequence records.

Consequently, a Y:A ratio could not be calculated.

The absence of a Y chromosome from the selected reference assembly does not establish that the WGS donor lacks a Y chromosome.

### 9.4 Dosage Interpretation

<details>
<summary>Result summary</summary>

```text
Median autosome depth: 9.673
X / A ratio: 0.974
Y / A ratio: NA
Dosage interpretation: XX-like
```

</details>

The observed X:A ratio of 0.974 exceeds the classroom threshold of 0.80 and is close to the expected ratio for two X-chromosome copies relative to the autosomes.

Therefore, the R analysis produced an **XX-like dosage inference**.

This is a read-depth-based inference and should not be interpreted as definitive cytogenetic confirmation of an XX karyotype.

## 10. Chromosome-Depth Figure

The following figure represents the relative sequencing depth of the autosomes and X chromosome.

![Chromosome depth analysis](results/chromosome_depth.png)

The y-axis represents chromosome depth relative to the median autosomal depth.

A relative depth near 1.0 indicates sequencing depth close to the autosomal median. The X chromosome has a relative depth of approximately 0.974, which is consistent with the XX-like interpretation produced by the classroom analysis script.

## 11. Answers to the Laboratory Questions

### Question 1. What species did you choose, and what evidence supports a diploid XX/XY or ZZ/ZW system?

The selected species was *Equus caballus* (horse). The horse has a conventional mammalian XX/XY sex-chromosome system. Females typically possess two X chromosomes (XX), while males typically possess one X and one Y chromosome (XY). The EquCab3.0 chromosome-level assembly identifies 31 autosomes and an X chromosome, supporting the identification of the X chromosome for the dosage analysis.

### Question 2. What are your assembly accession, WGS run, and both BioSample accessions? Are the donors the same?

The reference assembly was EquCab3.0, with RefSeq accession **GCF_002863925.1** and assembly BioSample **SAMN02953672**.

The WGS run was **SRR25750664**, with WGS BioSample **SAMN37129746**.

The assembly and WGS BioSamples are separate records. The donors were therefore treated as different individuals in this analysis.

### Question 3. Which sequences were used as autosomes and as X or Z? How did you verify their identities?

The 31 autosomes were identified using RefSeq accessions **NC_009144.3 through NC_009174.3** and were assigned to group A.

The X chromosome was identified as **NC_009175.3** and assigned to group X.

Their identities were verified using the NCBI EquCab3.0 assembly report and by matching the exact sequence identifiers with the reference names in the Samtools Coverage output.

Mitochondrial DNA, unplaced scaffolds, and other non-autosomal sequences were excluded from the autosomal group.

### Question 4. What are the median autosomal depth, X:A or Z:A ratio, and inferred sex-chromosome complement?

The median autosomal sequencing depth was **9.673×**, and the X:A ratio was **0.974**.

The ratio is close to the expected value of approximately 1.0 for an XX complement. According to the classroom interpretation guidelines, the result is therefore classified as **XX-like**.

The Y:A ratio was not available because the selected reference assembly did not contain an annotated Y chromosome in its primary chromosome-level records.

### Question 5. Does your result agree with the recorded sex of the WGS donor, if reported? Explain any discrepancy or uncertainty.

Yes. The WGS BioSample metadata reports the donor as female, and the read-depth analysis produced an XX-like dosage inference.

The two results are consistent. However, this agreement does not establish a definitive XX karyotype because read-depth analysis is an indirect method of estimating chromosome dosage.

The assembly donor and WGS donor were treated as different individuals. Therefore, the WGS result should be compared with the WGS donor's metadata rather than automatically attributed to the assembly donor.

Potential sources of uncertainty include mapping bias, repetitive sequences, pseudoautosomal regions, sequencing-depth variation, reference representation, and differences in chromosome-specific coverage.

### Question 6. Why is a chromosome-level assembly alone insufficient for a reliable read-depth sex inference?

A chromosome-level assembly provides reference sequences and chromosome identities, but it does not measure the sequencing depth of the actual WGS donor.

Sex-chromosome dosage inference requires sequencing reads from the sample to be aligned to the reference genome and the resulting chromosome-specific coverage to be compared with autosomal coverage.

Factors such as low sequencing depth, mapping bias, repetitive DNA, pseudoautosomal regions, incomplete reference representation, and unusual karyotypes can influence the observed ratios.

Therefore, chromosome-level assembly information alone is insufficient to determine the sex-chromosome complement of an individual using read-depth analysis.

## 12. Limitations and Sources of Uncertainty

Several limitations must be considered when interpreting the results.

1. **Different biological samples:** The assembly BioSample and WGS BioSample are separate records and were treated as different individuals.

2. **Absence of an annotated Y chromosome:** The selected reference assembly does not contain an annotated Y chromosome among its primary chromosome-level sequences. Therefore, a Y:A ratio could not be calculated.

3. **Indirect dosage estimation:** The X:A ratio estimates relative chromosome dosage from sequencing coverage. It does not directly determine the individual's karyotype.

4. **Mapping bias:** Differences in sequence similarity between the WGS reads and reference genome can affect chromosome-specific alignment and coverage.

5. **Repetitive sequences:** Repetitive genomic regions can complicate read mapping and influence measured depth.

6. **Pseudoautosomal regions:** These regions share sequence homology between X and Y chromosomes and may affect chromosome-specific mapping behavior.

7. **Coverage variation:** Sequencing depth may differ among chromosomes because of technical and biological factors.

8. **Reference representation:** An absent Y sequence in the selected reference does not prove that the WGS individual lacks a Y chromosome.

9. **Classroom thresholds:** The interpretation thresholds are instructional guidelines and should not be treated as validated diagnostic criteria.

10. **Unusual chromosomal complements:** Atypical karyotypes or sex-chromosome abnormalities may produce read-depth patterns that differ from the expected XX and XY models.

The XX-like result must therefore be interpreted as a dosage inference from the available sequencing data, not as definitive biological sex determination.

## 13. Conclusion

This project used whole-genome sequencing read-depth analysis to estimate X-chromosome dosage in *Equus caballus* using the EquCab3.0 reference assembly.

Paired-end WGS reads from run SRR25750664 were imported into Galaxy, evaluated using FastQC and MultiQC, and aligned to the reference genome using BWA-MEM2. Chromosome-specific coverage was subsequently calculated using Samtools Coverage with a minimum mapping quality of 20 and minimum base quality of 20.

The resulting coverage data were analyzed using a base-R script. The median autosomal sequencing depth was **9.673×**, and the calculated X:A ratio was **0.974**.

According to the classroom interpretation guidelines, the result corresponds to an **XX-like sex-chromosome dosage**. This inference agrees with the female sex reported in the WGS BioSample metadata.

However, the selected reference assembly lacks an annotated Y chromosome in its primary chromosome-level sequence records, preventing calculation of a Y:A ratio. The assembly and WGS donors were also treated as different individuals.

Overall, the analysis demonstrates how whole-genome sequencing read depth can be used to estimate sex-chromosome dosage while emphasizing the importance of reference-genome representation, sequencing quality, chromosome-specific coverage, and careful biological interpretation.

## 14. Repository Structure

The GitHub repository is organized as follows:

```text
horse-sex-chromosome-dosage-analysis/
│
├── README.md
│
├── chromosome_groups.csv
│
├── chromosome_coverage.tsv
│
├── sex_depth_analysis.R
│
├── results/
│   ├── chromosome_relative_depth.csv
│   ├── chromosome_depth.png
│   └── sex_inference.txt
│
└── evidence/
    ├── Adapter_Content.png
    ├── BWA_Alignment.png
    ├── Forward_FastQC-webpage.pdf
    ├── MultiQC_Statistics.png
    ├── NCBI_BioSample_Sex_Verification.png
    ├── NCBI_SRA_Run_Metadata.png
    ├── Per_Base_Sequence_Quality.png
    ├── Per_Sequence_GC_Content.png
    ├── R_Analysis_Console.png
    ├── Reverse_FastQC-webpage.pdf
    ├── Samtools_Coverage_Preview.PNG
    └── Samtools_Flagstat.png
```

The repository contains the smaller analysis outputs, chromosome grouping file, R script, results, and supporting evidence.

Large sequencing and alignment files were intentionally excluded from GitHub:

- FASTQ files
- Reference FASTA files
- BAM files
- CRAM files

These files are retained in the appropriate analysis environment rather than being uploaded to the repository.

## 15. Supporting Evidence

### NCBI Records

**WGS BioSample metadata**

![NCBI BioSample sex verification](evidence/NCBI_BioSample_Sex_Verification.png)

**SRA run metadata**

![NCBI SRA run metadata](evidence/NCBI_SRA_Run_Metadata.png)

### Sequencing Quality Control

**MultiQC statistics**

![MultiQC statistics](evidence/MultiQC_Statistics.png)

**Per-base sequence quality**

![Per-base sequence quality](evidence/Per_Base_Sequence_Quality.png)

**Per-sequence GC content**

![Per-sequence GC content](evidence/Per_Sequence_GC_Content.png)

**Adapter content**

![Adapter content](evidence/Adapter_Content.png)

The complete forward and reverse FastQC reports are also included:

- [Forward FastQC report](evidence/Forward_FastQC-webpage.pdf)
- [Reverse FastQC report](evidence/Reverse_FastQC-webpage.pdf)

### Alignment and Coverage

**BWA-MEM2 alignment**

![BWA-MEM2 alignment](evidence/BWA_Alignment.png)

**Samtools Flagstat**

![Samtools Flagstat](evidence/Samtools_Flagstat.png)

**Samtools Coverage output**

![Samtools Coverage preview](evidence/Samtools_Coverage_Preview.PNG)

### R Analysis

**R analysis console**

![R analysis console](evidence/R_Analysis_Console.png)

**Chromosome-depth analysis**

![Chromosome depth results](results/chromosome_depth.png)

## 16. References

1. National Center for Biotechnology Information (NCBI). *Equus caballus* EquCab3.0 reference genome assembly. RefSeq accession GCF_002863925.1. [NCBI Assembly](https://www.ncbi.nlm.nih.gov/datasets/genome/GCF_002863925.1/).

2. National Center for Biotechnology Information (NCBI). Assembly BioSample SAMN02953672. [NCBI BioSample](https://www.ncbi.nlm.nih.gov/biosample/SAMN02953672).

3. National Center for Biotechnology Information (NCBI). Whole-genome sequencing run SRR25750664. [NCBI SRA](https://www.ncbi.nlm.nih.gov/sra/SRR25750664).

4. National Center for Biotechnology Information (NCBI). WGS BioSample SAMN37129746. [NCBI BioSample](https://www.ncbi.nlm.nih.gov/biosample/SAMN37129746).

5. National Center for Biotechnology Information (NCBI). BioProject PRJNA1005486. [NCBI BioProject](https://www.ncbi.nlm.nih.gov/bioproject/PRJNA1005486).

6. Galaxy Project. [Galaxy platform](https://usegalaxy.org/).

7. Samtools. [Samtools documentation](https://www.htslib.org/doc/samtools.html).

8. Cell and Molecular Biology. Individual Practical Exercise: **Sex-Chromosome Dosage in a Selected Animal Nuclear Genome Using NCBI, Galaxy, and R.** Laboratory manual.


