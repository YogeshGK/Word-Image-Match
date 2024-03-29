# Word Image Match
<img src="./img/header.jpeg" alt="Stroke" height="350" width="700">

## George Washington's Letters Image Matching
### Problem Statement
This project tackles a fascinating machine learning problem centered around George Washington's letters. The dataset comprises images, each containing a single English word. Additionally, there is a ground truth providing information about which word is present in each image. The ultimate goal is to develop a solution that accurately identifies the image file in the dataset that corresponds to a given word.

### Data Preprocessing
The initial steps involved cleaning the ground truth data. This included handling underscores, numbers, and other specific processing requirements. On the image side, a thorough preprocessing approach was taken. To ensure consistency, all images were resized to the maximum height and width found in the dataset. This involved zero-filling to match dimensions, resulting in a standardized format. The images were then converted into 1D arrays, streamlining the subsequent steps.

### Dataset Splitting
The dataset was split into training and testing sets. This segregation was crucial for evaluating the model's performance on unseen data.

### Nearest Neighbor Algorithm
The core of the solution lies in the application of the nearest neighbor algorithm, with the cosine metric chosen for its effectiveness in this context. The algorithm was first executed on the training dataset. The resulting model, trained on the characteristics of the dataset, was then applied to the test dataset.

### Computes various features from binary images.
-  Sum of ones per column
-  First occurrence of 1 when scanning from top to bottom
-  First occurrence of 1 when scanning from bottom to top
-  First occurrence of 1 when scanning from left to right
-  First occurrence of 1 when scanning from right to left

### Matching Process
Upon running the algorithm on the test dataset, it produced indices corresponding to the closest matching images in the training dataset. These indices serve as references, allowing a lookup in the training dataset to find the images most closely related to the input image from the test dataset.

### Pre-requisites  
To run the code in Google collab, 
- copy the contents of ./data folder to on gdrive and mount it and provide its location in PATH.
- copy the contents of ./ground_truth/word_labels.txt to another folder and give the path in GROUND_TRUTH_FILE
- create one more folder and provide the path in PADDED_PATH. we will store image after preprocessing here.

### Results 

| Model | Accuracy | 
|----------|----------|
| kNN| 1% |
| kNN with Features| 0.7% |
| Hist. Oriented Gradient| 4% |
| Local Binary Pattern| 4% |

### Future Enhancements
1. Implement deep learning approaches for image matching.
2. Utilize vector database

## Badges
[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)
![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?style=for-the-badge&logo=TensorFlow&logoColor=white)

