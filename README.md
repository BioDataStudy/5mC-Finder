# 5mC-Finder
5mC-Finder: Deciphering the location and consensus patterns of RNA 5-methyluridine sites by deep learning

RNA 5-methyluridine (m5U) represents an essential post-transcriptional RNA modification, which is crucial for modulating various biological functions and disease pathogenesis, such as breast cancer development. Accurate identification of the m5U sites in the transcriptome and their consensus RNA motifs will yield insights into its biological functions and mechanisms.We systematically estimated the predictive power of 12 sequence features and developed the first deep learning based tool, named m5U-Finder, to capture sophisticated regulatory patterns for predicting m5U modification sites de novo from RNA sequences. In comparison, m5U-Finder outperforms 84 conven-tional machine-learning predictors, with the area under curve (AUC) value greater than 0.97 in 10-fold cross-validations and independent test. By interpreting and visualizing the sequence features deciphered by m5U-Finder, we identify novel RNA motifs for m5U modification.

# Installation
Download 5mC-Finder by
```
git clone https://github.com/BioDataStudy/5mC-Finder
```
Installation has been tested in Linux with Python 3.7.
Since the package is written in python 3x, python3x with the pip tool must be installed.
5mC-Finder uses the following dependencies: numpy, scipy, pandas, h5py, keras version=2.3.1, tensorflow=1.15. You can install these packages by the following commands:
```
pip install pandas
pip install numpy
pip install scipy
pip install h5py
pip install -v keras==2.3.1
pip install -v tensorflow==1.15
```

# Performance
m5U-Finder outperforms 84 conventional machine-learning predictors, with the area under curve (AUC) value greater than 0.97 in 10-fold cross-validations and independent test.

![image](https://github.com/BioDataStudy/5mC-Finder/blob/2d195b681b89259e738c0ba3bcce5dee25c2c08e/prediction/performance.png)

# Interpretability
To decipher the capability of the hierarchical representation and learning, we visualized the m5U and non-m5U sites using UMAP (Uniform Manifold Approximation and Projection) method based on the feature representations uncovered at different network layers. the learned features turn into more and more discriminative along the layer hierarchy, with m5U and non-m5U sites mixed at the input layer without clear boundary, culminating with a clear separation in the output layer.

![image](https://github.com/BioDataStudy/5mC-Finder/blob/99a4038ca69585ac5e23dae074a9f296d66850d7/umap/Uamp_testing.png)

# Motifs
The kernels in the first convolutional layer distinguish important weight matrices over the input sequences to recognize significant patterns. Therefore, we decoded all filters in the convolutional layer of 5mU-Finder and converted them into motifs. As a result, a total of 135 informative motifs were characterized, and several novel RNA mo-tifs with the consensus sequence were discovered, such as CxGGGAxC and GGGxUCG. The clustering analysis of the informative motifs re-vealed their enrichments and higher distributions in positive instances .

![image](https://github.com/BioDataStudy/5mC-Finder/blob/main/motif/Figure%202.jpg)

# Usage
Please cd to the 5mC-Finder/prediction/ folder which contains predict.py.
Example: 
```
python predict.py -f ../testdata/test.fasta -o ../testdata/test_result.txt
```
For details of other parameters, run:
```
python predict.py --help
```

# Citation
Please cite the following paper for using: Deciphering the location and consensus patterns of RNA 5-methyluridine sites by deep learning. Submission 2021.
