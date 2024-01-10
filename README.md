# Word Image Match

## George Washington's Letters Image Matching
### Problem Statement
This project tackles a fascinating machine learning problem centered around George Washington's letters. The dataset comprises images, each containing a single English word. Additionally, there is a ground truth providing information about which word is present in each image. The ultimate goal is to develop a solution that accurately identifies the image file in the dataset that corresponds to a given word.

### Data Preprocessing
The initial steps involved cleaning the ground truth data. This included handling underscores, numbers, and other specific processing requirements. On the image side, a thorough preprocessing approach was taken. To ensure consistency, all images were resized to the maximum height and width found in the dataset. This involved zero-filling to match dimensions, resulting in a standardized format. The images were then converted into 1D arrays, streamlining the subsequent steps.

### Dataset Splitting
The dataset was split into training and testing sets. This segregation was crucial for evaluating the model's performance on unseen data.

### Nearest Neighbor Algorithm
The core of the solution lies in the application of the nearest neighbor algorithm, with the cosine metric chosen for its effectiveness in this context. The algorithm was first executed on the training dataset. The resulting model, trained on the characteristics of the dataset, was then applied to the test dataset.

### Matching Process
Upon running the algorithm on the test dataset, it produced indices corresponding to the closest matching images in the training dataset. These indices serve as references, allowing a lookup in the training dataset to find the images most closely related to the input image from the test dataset.

### Pre-requisites  
To run the code in Google collab, 
- copy the contents of ./data folder to on gdrive and mount it and provide its location in PATH.
- copy the contents of ./ground_truth/word_labels.txt to another folder and give the path in GROUND_TRUTH_FILE
- create one more folder and provide the path in PADDED_PATH. we will store image after preprocessing here.


### Future Enhancements
Experiment with different distance metrics and algorithms to enhance accuracy.
Implement deep learning approaches for image matching.
Explore ways to optimize and speed up the image preprocessing steps.