# Alzheimer-gene-expression-classifier
*A preliminary bioinformatics and machine-learning analysis of GSE5281 gene-expression data, including differential expression analysis, biological interpretation, and an interactive Gradio prediction interface [Small sample omics-ML]*

## **Background**

Alzheimer's disease is a progressive neurodegenerative disorder involving widespread changes in neuronal function and molecular pathways. Identifying genes whose expression changes in the Alzheimer's brain may help reveal biological processes associated with disease-related neuronal dysfunction. In this study, we analyzed gene-expression profiles from the GSE5281 Alzheimer's disease dataset to identify candidate molecular changes associated with the disease.

## **Methods**

We analyzed a selected set of 10 brain samples from the GSE5281 dataset, comprising five Alzheimer's disease and five control samples. Probe identifiers were mapped to gene names using the GPL570 platform annotation, and the 100 most variable genes were selected for analysis. Expression values were log2-transformed, followed by fold-change calculation and independent-samples t-tests. A Logistic Regression classifier was then trained to distinguish Alzheimer's from control samples.

## **Results**

The volcano plot particularly highlights RPS3A, HECTD1, MAPK1, and GAD1 based on their fold-change positions, while the broader biological interpretation additionally considers UQCC2. These genes relate to inhibitory neurotransmission, intracellular signaling, neuronal structure, protein synthesis, neuronal protein biology, and gene regulation. None of the highlighted genes crossed the nominal p < 0.05 threshold in this small analysis.

The Logistic Regression model achieved 100% average training accuracy but an average 70% test accuracy. Across repeated train/test splits, test accuracy ranged from 50% to 100%, with a standard deviation of 16.96 percentage points, demonstrating substantial instability in performance.

## **Limitations**

The analysis is limited by the very small sample size and the high-dimensional feature space. With only 10 samples and 100 gene-expression features, the classifier is highly susceptible to overfitting, and the observed test performance cannot be interpreted as clinical diagnostic accuracy.

## **Conclusion**

This project helped us explore how gene-expression changes in Alzheimer's disease can be studied using bioinformatics and machine learning. 

The machine-learning model could separate the Alzheimer's and Normal samples very well during training, but its performance on unseen samples was much less stable. This showed me an important lesson: **a model can perform extremely well on a small dataset without necessarily being reliable on new patients.**

Overall, this project was not about building a diagnostic tool. It was about understanding the complete journey from **raw gene-expression data → biological interpretation → machine learning → model evaluation**, and seeing how computational methods can help us investigate complex diseases like Alzheimer's.


## **Future development**:

-Larger Alzheimer's cohorts

-Independent external validation

-Cross-validation

-Comparison of Logistic Regression, SVM, Random Forest and other classifiers

-SHAP-based model interpretation
