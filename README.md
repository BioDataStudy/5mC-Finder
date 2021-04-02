# 5mC-Finder
5mC-Finder: Deciphering the location and consensus patterns of RNA 5-methyluridine sites by deep learning

RNA 5-methyluridine (m5U) represents an essential post-transcriptional RNA modification, which is cru-cial for modulating various biological functions and disease pathogenesis, such as breast cancer devel-opment. Accurate identification of the m5U sites in the transcriptome and their consensus RNA motifs will yield insights into its biological functions and mechanisms.We systematically estimated the predictive power of 12 sequence features and developed the first deep learning-based tool, named m5U-Finder, to capture sophisticated regulatory patterns for predicting m5U modification sites de novo from RNA sequences. In comparison, m5U-Finder outperforms 84 conven-tional machine-learning predictors, with the area under curve (AUC) value greater than 0.97 in 10-fold cross-validations and independent test. By interpreting and visualizing the sequence features deciphered by m5U-Finder, we identify novel RNA motifs for m5U modification.

# Performance
m5U-Finder outperforms 84 conven-tional machine-learning predictors, with the area under curve (AUC) value greater than 0.97 in 10-fold cross-validations and independent test.

![image](https://github.com/BioDataStudy/5mC-Finder/blob/88eb55a50c08edb0a85ca75924ece71e1a6fb9ab/prediction/Slide1.jpg)

# Interpretability
To decipher the capability of the hierarchical representation and learning, we visualized the m5U and non-m5U sites using UMAP (Uniform Mani-fold Approximation and Projection) method based on the feature repre-sentations uncovered at different network layers. the learned features turn into more and more discriminative along the layer hierarchy, with m5U and non-m5U sites mixed at the input layer without clear boundary, culminating with a clear separation in the output layer.

![image](https://github.com/BioDataStudy/5mC-Finder/blob/88eb55a50c08edb0a85ca75924ece71e1a6fb9ab/prediction/Slide1.jpg)

# Usage
m5U-Finder outperforms 84 conven-tional machine-learning predictors, with the area under curve (AUC) value greater than 0.97 in 10-fold cross-validations and independent test.
