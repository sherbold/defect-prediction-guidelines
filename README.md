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

- Project
- Release
- Feature
- Bug / Defect
- Training Data (incl. Validation Data)
- Test Data
- Binary Classifier and Scoring Classifier (does this belong here?)

# Taxonomy

In the two decades, defect prediction evolved into a broad field with many different variants of how experiments are conducted. Sometimes it becomes are to distinguish between the variants - or even be aware of all of them. The goal of this section is specify fixed terminology for the different flavors of defect prediction in a taxonomy. 

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

