This repository is to provide the dataset and code to the article 'Uncovering the prognostic gene signatures for the improvement of risk stratification in cancers by using deep learning algorithm coupled with wavelet transform'. Please note that this code is ONLY provided for academic use.

File list:
1) data/Dataset_OV.xlsx:   The data of OV that has been divided into the training set and the test set. Could be used for Risk score model building.

2) data/OV_finalMatrix.tsv:   The gene expression data that includes all the samples of OV. Could be used for SWT-CNN model building with file 3).

3) data/OV_clinical.csv:   The label of samples of OV, indicates the classification of 3-year overall survival. Could be used for SWT-CNN model building with file 2).   

4) data/Dataset_OV_clinical.xlsx:   The overall_survival information and label of samples of OV. And samples of the training set and the test set are correspond to the file 1).

5) SWT-CNN_model.ipynb:   The code for SWT-CNN model building in our article.

6) Risk_score Method.ipynb:   The code for Risk score model building in our article.

7) Univariate Cox regression+Multivariable Cox regression.txt:   The code for performing the univariate cox regression and multivariable cox regression on the top n genes.

8) Univariate Cox regression+Penalized Cox regression.txt:   The code for performing the univariate cox regression and penalized cox regression on the top n genes.


Note:   
1) Files 5) and 6) need to be opend with jupyter notebook.
            
2) Files 7) and 8) are written in the R language.
            
3) The code for Risk score model building yield a file named OV_top1000Gene.csv eventually. And the file named OV_top1000Gene.csv could be used for cox regression analysis.
            
4) Choose file 7) or file 8) for cox regression analysis. And a file named OV_clinical_MultipleResult.csv will yield eventually.
            
5) The last cell of file 6) could be used for the calculation of risk score. The input file named OV_clinical_MultipleResult_0.05.csv was genes with p<0.05 in the OV_clinical_MultipleResult.csv.
    And a file named OV_cox0.05_Sample_score.xlsx will yield finally. It shows the risk score of each samples of the training set and the test set.

6) At last, file 4) combined with OV_cox0.05_Sample_score.xlsx could be used for classification ("Cox proportional-hazards regression" in the METHOD part in our article) .
    Receiver operating characteristics curve (ROC) could employed by the SPSS software.

Python model requirement:
1) xlrd
2) pyWavelet
3) keras
4) tensorflow-gpu
5) pandas
6) numpy
7) sklearn 
Note:  The code files 5) and 6) are recommend execute on GPUs.