# CNN with 7-Fold Cross-Validation

## Overview
This repository contains a Convolutional Neural Network (CNN) implementation with 7-fold cross-validation for robust model evaluation. The CNN is specifically designed for malaria parasite classification but can be used for image classification tasks and includes data preprocessing, model training, and evaluation scripts.

## Features
- 7-fold cross-validation for reliable performance estimation
- Customizable CNN architecture
- Support for various image datasets
- Training and evaluation metrics tracking
- Model saving and loading capabilities

## Dataset
The model was developed using the NIH malaria dataset, which can be downloaded from Kaggle.

Dataset URL: https://www.kaggle.com/datasets/iarunava/cell-images-for-detecting-malaria

### Dataset Structure
The dataset should be organized in the following structure:
```
dataset/
    ├── Parasitized/
    │   ├── ...
    ├── Uninfected/
    │   ├── ...
```

## Requirements
- Python 3.6+
- TensorFlow 2.x
- Keras
- NumPy
- scikit-learn
- Matplotlib (for visualization)

## Installation and usage
1. Download or clone this repository
2. extract the 'malaria_CNN_7-fold_validation.ipynb' file
3. copy to a location on your computer
4. Download the dataset from https://www.kaggle.com/datasets/iarunava/cell-images-for-detecting-malaria/data.
6. start terminal at that folder
7. Type jupyter notebook in the terminal
8. navigate to running malaria_CNN_7-fold_validation.ipynb notebook
9. find this line of code
    ```data_generator = datagen.flow_from_directory(directory='malaria_dataset_folder'...```
11. change **malaria_dataset_folder** to the name of the folder containing the dataset
12. Run and see changes


## 7-Fold Cross-Validation Process
The implementation performs the following steps:
1. Splits the dataset into 7 stratified folds
2. Trains the model on 6 folds and validates on the remaining fold
3. Repeats the process for all 7 combinations
4. Calculates average performance metrics across all folds

## Results
After training, the following will be saved in the output directory:
- Model weights for each fold
- Training history plots
- Performance metrics summary
- Confusion matrices

## License
MIT License

## Acknowledgments
I. Arunava . "Malaria Cell Images Dataset," Kaggle. [Online]. Available: https://www.kaggle.com/datasets/iarunava/cell-images-for-detecting-malaria/data.
National Library of Medicine. "Downloadable Data: Malaria Datasets," Lister Hill National Center for Biomedical Communications (LHNCBC). [Online]. Available: https://lhncbc.nlm.nih.gov/LHC-downloads/downloads.html#malaria-datasets.
