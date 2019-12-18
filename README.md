![Udacity Logo](./docs/img/udacity-logo.svg)

# Machine Learning Engineer Nanodegree 
## Capstone Project
## Landmark Recognition

> ### Fady Morris Milad Ebeid  
> ### December 13, 2019

Computer vision algorithms include methods for acquiring, processing, analyzing and understanding digital images, and extraction of data from the real world. It is an interdisciplinary field that deals with how can computers gain a high-level understanding of digital images. It aims to mimic human vision.  
Convolutional neural networks are now capable of outperforming humans on some computer vision tasks,
such as classifying images.  
In this project, I provide a solution to the Landmark Recognition Problem. Given an input photo of a place anywhere around the world, the computer can recognize and label the landmark in which this image was taken.

# Udacity Nanodegree Program Graduate Certificate
**Credential ID:** 57A56H32  
**Certificate Link :** [https://graduation.udacity.com/confirm/57A56H32](https://graduation.udacity.com/confirm/57A56H32)  
(Certificate earned at Monday, December 15, 2019)  
![Certificate](https://s3-us-west-2.amazonaws.com/udacity-printer/production/certificates/a010e1e1-a8f5-43e3-a352-5898b7ad1ef0.svg)

# Libraries Used
- [Python 3.x](https://www.python.org)
- [NumPy](https://numpy.org/)
- [Pandas](https://pandas.pydata.org/)
- [Tensorflow](https://www.tensorflow.org)
- [Keras](https://keras.io)


# Directory Structure

  
- [notebooks/](./notebooks/) : Contains the project Jupyter notebooks and exported HTML files of the project notebooks.  
- [src/](./src/) : Contains python helper scripts.
- [docs/](./docs/) : Contains the project [report](./docs/report.pdf) and [proposal](./docs/proposal.pdf).  
   
   
**Full project directory structure :**
```
<project root directory>
├── README.md                                            - Project readme file.
├── notebooks/
│   ├── data_exploration_and_preprocessing.ipynb         - Code for dataset download and preprocessing.
│   └── Udacity_MLND_capstone_landmark-recognition.ipynb - Project implementation.
├── src/
│   └── image_downloader.py                              - Python helper script to download images.
├── docs/                     - Project documentation directory.
│   ├── proposal.pdf          - Project proposal.
│   ├── report.pdf            - Project report.
│   ├── figures/              - Project output plots and graphs.
│   ├── img/                  - Project logos and other images. 
│   └── stats/                - Project output statistics, metrics, and dataset summary.
├── data/                           
│   ├── processed/                       - Project downloaded and processed dataset.
│   │   ├── index_train.csv
│   │   ├── index_validation.csv
│   │   ├── index_test.csv
│   │   ├── train/
│   │   ├── validation/
│   │   └── test/
│   ├── raw/                             - Raw Google Landmarks dataset CSV files.
│   │   ├── train.csv
│   │   └── train_label_to_category.csv
│   └── test_images/                     - Unseen test images downloaded from the web.
│       └── files/
└── models/     - Project saved training best weights, training history and bottleneck features
```




# Project Directory and Data Preparation

- Clone the repository :

        git clone https://github.com/FadyMorris/udacity-mlnd-capstone-landmark-recognition.git

- Download the processed dataset archive `data_processed.tar.gz` from this [Google Drive link](https://drive.google.com/open?id=1k9zJ23fMfEBk1XzAsRYAJQjK9cpYSQTr), then extract it to the project root directory.  
This is a subset dataset that was extracted from Common Visual Data Foundation [Google Landmarks Dataset v2](https://github.com/cvdfoundation/google-landmark).
- (Optional): You can download the output from previous run of the model,`models.tar.gz` and `stats.tar.gz` from [Google Drive link](https://drive.google.com/open?id=1k9zJ23fMfEBk1XzAsRYAJQjK9cpYSQTr) and extract them to the project root directory.  
If you don't download these files, run the following commands to create the output directories:

        cd udacity-mlnd-capstone-landmark-recognition
        mkdir models
        mkdir -p docs/figures
        mkdir -p docs/stats
        
- (Optional): If you want to run [data_exploration_and_preprocessing notebook](./notebooks/data_exploration_and_preprocessing.ipynb) to create your own dataset, download [train.csv](https://s3.amazonaws.com/google-landmark/metadata/train.csv) and [train_label_to_category.csv](https://s3.amazonaws.com/google-landmark/metadata/train_label_to_category.csv) and place them inside `data/raw/` directory. These are raw index files from Common Visual Data Foundation [Google Landmarks Dataset v2](https://github.com/cvdfoundation/google-landmark).
- Download your test images and place them inside `data/test_images/files/` directory.
