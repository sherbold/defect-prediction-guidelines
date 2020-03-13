# Introduction

The goal of this repository is to create shared and agreed upon best practices for defect prediction research. Suggestions for contributions can be made by anyone in the research community by creating and issue or submitting a pull request. These guidelines is to cover the following aspects to improve the way defects prediction experiments are conducted and the results are reported. The goal is that these guidelines will cover the following aspects:

- A taxonomy that defines the different defect prediction flavors.
- How training and test data should be used for the different flavors of defect prediction.  
- Requirements on the data needed to conduct studies including quality assurance for the data. 
- Performance criteria to be used for evaluations.
- Statistical tests and visualizations.
- Reporting of results.
- Threats to validity that should be considered.
- Replication kits.

These guidelines are still a work-in-progress and not all aspects are covered yet. Once stable, we consider submitting the guidelines for review to a journal, e.g., Empirical Software Engineering and will invite everyone who significantly contributed (i.e., suggest content, helped to improve the guidelines) to co-author the manuscript. 

# Terminology

Within this section, we establish basic terminology, including often used synonyms.


| Term | Description | Notation |
-------|-------------|----------|
| Project | A software project that consists of well-defined scope, typically hosted in a single repository. |
| Release | The release of a software project, e.g., version 1.0.0, version 2.1.1 | S |
| Version | Often used synonymously with the term release, although version is a bit more generic and can also refer to milestones or release candidates. | S |
| Artifact | The part of a software project to which defect prediction is applied. Typically a file or a class, but possibly also a commit, or even a part of a commit. | s &isin; S|
| Defect / Bug / Fault | An imperfection or deficiency in a work product where it does not meet its requirements or specifications. Source: [ISTQB Glossary] |
| Pre-release Defect  | A defect that was found and fixed prior to a release. |
| Post-release Defect | A defect that was found and fixed after the software released. |
| Feature | A measurement of related to an artifact that is used as input for a classifier and the foundation for a prediction. |
| Feature set | A collection of measurements for software artifacts. |
| Feature space | A (usually) real-valued space that is defined by the measurements of artifacts according to the feature set. |
| Binary Label | The label assigned to artifacts depending on whether artifact is defective or not. | {True, False}  |
| Defect Count | An integer version of the label that assigns the number of defects as the label. |  |
| Binary Classifier | A classifier that predicts if an artifact is defective or not. |  |
| Scoring Classifier | A classifier that predicts a score for each artifact and can rank artifacts by their scores. |
| Threshold | A fixed value used to transform the scores of a scoring classifier into binary labels, i.e., to make a scoring classifier into a binary classifier. All artifacts with values above the threshold are predicted as defective. |
| Training Data |  |
| Validation Data | |
| Test Data | |

(1): Sometimes also {+1, -1} if this is relevant for the definition of loss function of the learning problem. 

# Taxonomy

In last the two decades, defect prediction evolved into a broad field with many different variants of how experiments are conducted. Sometimes it becomes hard to distinguish between the variants - or even be aware of all of them. The goal of this section is specify fixed terminology for the different flavors of defect prediction in a taxonomy. 

- Defect Prediction
  - Release-level Defect Prediction
    - Within-Project Defect Prediction
      - Cross-Validation Experiments
      - Semi-Supervised Defect Prediction
      - Cross-Version Defect Prediction
    - Mixed-Project Defect Prediction
    - Cross-Project Defect Prediction
      - Strict Cross-Project Defect Prediction
      - Mixed Cross-Project Defect Preidction
      - Heterogeneuous Defect Prediction
  - Just-in-time Defect Prediction
 
## Descriptions of the Types

### Release-level Defect Prediction

Defect prediction is applied to all artifacts at a specific points in time during software development processes, e.g., to releases or release candidates. The goal of release level defect prediction is to guide the quality assurance efforts, i.e., focus testing efforts on the predicted artifacts. In the literature, the artifacts are typically modules, files, or classes, although methods were also already considered. 

# Training and Test Data

- Should possibly be joined with Taxonomy to avoid redundancies

# Data Selection

- How to select (and not select!) subsets from public data sets
- How to sample projects for new data

# Performance Criteria

- Which metrics are suitable
- Depends to some degree on flavor of defect prediction

# Statistical Tests

- Comparison of multiple classifiers with different projects as test data --> paired samples
- Use Demsar's Guidelines
- ScottKnott not suitable, as this has an independence assumption, i.e., does not work with paired data (could potentially be modified o work with repeated measures ANOVA instead of ANOVA)
- Effect sizes, both parametric and non-parametric
 
# Summary Statistics

- Mean as central tendency and standard deviation for normally distributed performance values
- Median and either Median Absolute Deviation from the Median (MAD) or InterQuartile Range (IQR) 

# Visualization of Results

- Boxplots vs. Violinplots
- When and how to use jitter
- Maybe even errorbars for confidence intervals (?)

# Reporting Threats to Validity

# Sharing Code and Data in Replication Kits


[ISTQB Glossary]: https://glossary.istqb.org/
