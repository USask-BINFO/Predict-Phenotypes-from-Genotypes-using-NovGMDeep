# Predicting Phenotypes From Novel Genomic Markers Using Deep Learning
- - - 

Genomic selection (GS) is a potent method to enhance quantitative traits. Traditional GS methods have used Single Nucleotide Polymorphism (SNP) markers to predict phenotypes. However, they do not consider non-linearity between the variables and face challenges due to the high dimensionality of genome-wide SNP markers. GS can benefit from Deep learning (DL), which provides novel approaches to process noisy data and handle non-linearity. Moreover, non-SNP DNA variation, such as Structural Variations (SVs) and Transposable Elements (TEs), accounts for a smaller number of variation events comparing to SNPs, however they involve a much larger proportion of overall variant bases. Such novel genomic markers (SVs and TEs) could have more significant contribution to plant phenotypic diversity. Here, we present a one-dimensional deep convolutional neural network model for genomic selection, NovGMDeep, that predicts phenotypes using novel genomic markers to evade the curse of high dimensionality and non-linearity of traditional GS models. The model avoids overfitting by applying the convolutional, pooling, and dropout layers hence decreases the complexity caused by the large number of genomic markers. We trained and evaluated the model on the samples of Arabidopsis thaliana and Oryza sativa using K-Fold cross-validation. The prediction accuracy is evaluated using Pearson’s correlation coefficient (PCC), Mean absolute error (MAE), and Standard deviation of MAE. The predicted results for the phenotypes showed a higher correlation when the model is trained with SVs and TEs than with SNPs. NovGMDeep also has higher prediction accuracy when compared with traditional statistical GS models. This work sheds light on the unrecognized function of SVs and TEs in genotype-to-phenotype associations, as well as their extensive significance and value in crop development.

The following figure shows the developed model in this paper:   

![NovGMDeep Architecture](Pictures/NovGMDeep.png#center)  

# Installation
Python 3.9
```
pip install -r requirements.txt
```

# Data
The full VCF variant files containing the structural variants data for A. thaliana samples are publicly available on European Variation Archive https://www.ebi.ac.uk/ena/browser/view/ERZ1458872?show=analyses (PRJEB38975) \
The phenotype data of Flowering time of A. thaliana samples can be found in the file "FT10_arabi.csv"

# Usage
1. Data Preprocessing
> Script for selectiing good quality genotypes: quality_based_selection.ipynb
> Script for making the data input-ready to the model: data_processing.ipynb

2. Data Split
> Script for splitting training and testing datasets: sv_data_split.py  

3. Train the Model
> Script for training: sv_model_train.py  

4. Test the Model
> Script for testing: sv_model_train.py 

# Citation
```
@article{sehrawat2022predicting,
  title={Predicting Phenotypes From Novel Genomic Markers Using Deep Learning},
  author={Sehrawat, Shivani and Najafian, Keyhan and Jin, Lingling},
  journal={bioRxiv},
  year={2022},
  publisher={Cold Spring Harbor Laboratory}
}
```
