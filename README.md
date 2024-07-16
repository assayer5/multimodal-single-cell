## Project: Multimodal single cell NGS data

### Overview
Multimodal single cell NGS data (Multiome and CITE-seq) utilized for multioutput regression. For the CITE-seq dataset, scRNA-seq data is used to predict surface protein expression with ensemble model of boosted trees and regularized regression. For the Multiome dataset, ATAC-seq data is used to predict gene expression with a neural network.

### Some Details
This data was part of a machine learning challenge posted on Kaggle. I explored multimodal single cell NGS data and multiple machine learning models in the following notebooks.

>*multimodal-single-cell-eda.ipynb*
>
>I explore the metadata, inputs, and targets of the datasets.

CITE-seq combines single cell RNA-seq (scRNA-seq) data with surface protein expression data:
>*multimodal-single-cell-citeseq.ipynb*
>
>I transformed the data to sparse matricies and reduced the feature space with SVD. I used the metadata to add a feature indicating the day of the experiment. I also clustered data with k-means to use the cluster membership as a feature. With an ensemble model of Ridge regression and XGBoost, I trained the model to predict surface protein expression from the scRNA-seq and engineered features.

In the Multiome dataset, ATAC-seq data is used to predict gene expression:
>*pytorch-multimodal-single-cell-multiseq.ipynb*
>
>I scaled inputs and outputs by their maximums and added a feature from the available metadata. For the model, I defined a neural network, but the final network structure and training is still undetermined.

### Language
Python

### Packages Used
h5py, anndata, scanpy, scipy, sklearn, xgboost, pytorch

### Models
Ridge Regression and XGBoost

ANN

### Resources
[Kaggle](https://www.kaggle.com/)

[AnnData](https://anndata.readthedocs.io/en/latest/)

[Scanpy](https://scanpy.readthedocs.io/en/stable/)

[PyTorch Documentation](https://pytorch.org/docs/stable/index.html)
