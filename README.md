## Project: Multimodal single cell NGS data

### Overview
Multimodal single cell NGS data (Multiome and CITE-seq) utilized for multioutput regression. For the CITE-seq dataset, scRNA-seq data is used to predict surface protein expression with ensemble model of boosted trees and regularized regression. For the Multiome dataset, ATAC-seq data is used to predict gene expression with a neural network.

Model training ongoing...

### Language
Python

### Packages Used
h5py, anndata, scanpy, scipy, sklearn, xgboost, pytorch

### Preprocessing and Feature Engineering
CITE-seq
- transformed data to sparse matricies
- reduced feature space with SVD 
- clustered data with k-means

Multiome
- scaled inputs and outputs by maximums
- added feature from available metadata

### Models
Ridge Regression and XGBoost

ANN

### Resources
[Kaggle](https://www.kaggle.com/)

[AnnData](https://anndata.readthedocs.io/en/latest/)

[Scanpy](https://scanpy.readthedocs.io/en/stable/)

[PyTorch Documentation](https://pytorch.org/docs/stable/index.html)
