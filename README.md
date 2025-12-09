# Final DAEN 429 Project: ASL Visual Detection Model
This project evaluates sign-language recognition models using static American Sign Language (ASL) alphabet classification. Four training policies were tested: T-A (head only), T-B (last block + head), T-C (progressive unfreezing), and S-A (training from scratch). The goal is to compare model accuracy, F1 score, and generalization performance across different training strategies. 

### Dataset Overview

To use the data, edit the file paths defined in beginning of the code.
The 29-class ASL Alphabet was automatically downloaded from Kaggle. There were 87,000 training images, 28 test images, and 27 custom test images. The 29 classes consist of letters A-Z, “del”, “nothing”, and “space.”

To begin training, an 80/20 train/validation split was created, and class labels were identified. To improve generalization, we implemented data augmentations only on the training set. We implemented horizontal flips, rotations, translations, adjusted color and brightness, and added a Gaussian blur. The validation and test sets received no augmentations to ensure consistent evaluations. 


