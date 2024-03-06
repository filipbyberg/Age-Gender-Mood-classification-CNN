# Age-Gender-Mood-classification-CNN

![image](https://github.com/filipbyberg/Age-Gender-Mood-classification-CNN/assets/80341025/90446b40-30a8-413a-9ec7-5c99afa0981e)

## About
In ths project we explore the training of a 3 simple CNN models to train a predictor of Age, Gender and Mood application, based solely on a portrait input image of a face.
The project was set to collect data about customers entering a clothing store to see if they bought anything, identifying their age group, mood and gender, upon entering the store. The objective was to identify patterns of potential customer based on those attributes.

To see the full project, check out the Google collab: https://drive.google.com/drive/folders/1--4WrQ-E3YeXqGGMK5-scUwsWzh3_mWa?usp=sharing

## Dataset

For the application to be able to perform as accurately as possible, a good dataset with a lot of diversity and variety is necessary. The considerations that were taken, when choosing a dataset, was the following:
• Variety in ethnicity
• A wide age range
• Even gender distribution
• A variety of facial expressions
• Augmented/rotated face-images
To be able to represent all the criteria shown above, the two datasets; UTK Faces with 23 708 images, and Kaggle Facial Age with 9 778 images was chosen, resulting in a total of 33 486 images.

![image](https://github.com/filipbyberg/Age-Gender-Mood-classification-CNN/assets/80341025/ca439078-3954-45d7-ab9b-ff10decfe276)

UTK Faces and Facial Age datasets were combined to build the Age Detection model of the project. With these two datasets combined, there are around 34000 labelled facial images from age 1 to 116 to work with. Although we have about 34000 images, more than that is needed to train a neural network with good accuracy. For this reason, 70% of all data reserved for training has been expanded 10 times with the data augmentation technique.

![image](https://github.com/filipbyberg/Age-Gender-Mood-classification-CNN/assets/80341025/1e407ab1-b476-42da-b458-095574bba97f)

## Classification
Since age, mood and in some cases gender, can be difficult to determine even by humans, a limited selection of classes are made for each prediction model. This helps the program make more generalized decision when classifying each dataset. For the three prediction models, the following classes was made.

![image](https://github.com/filipbyberg/Age-Gender-Mood-classification-CNN/assets/80341025/fb413b53-1355-4c70-8ed5-e1fcc0f35be3)


## Training
![image](https://github.com/filipbyberg/Age-Gender-Mood-classification-CNN/assets/80341025/f2ea33f0-626b-4939-91e0-df4087a63a93)

Our age prediction CNN model shall be defined and trained by:

1. Importing training and test datasets from Google Drive Input Sub-folder (UTK and KAGGLE)
2. Training dataset is already augmented and has 234,000 images
3. Greyscaling images instead of using RGB color images
4. Defining our intuitively distributed classes of age-ranges / different moods / Gender
5. Using 20 epochs on our optimized CNN Architecture, comprising of:
  - an input Conv2D layer (with 32 filters) paired with an AveragePooling2D layer,
  - 3 pairs of Conv2D (with 64, 128 & 256 filters) and AveragePooling2D layers,
  - a GlobalAveragePooling2D layer,
  - 1 Dense layer with 132 nodes, and
  - an output Dense layer with 7 nodes.

## Result

![image](https://github.com/filipbyberg/Age-Gender-Mood-classification-CNN/assets/80341025/8c878694-28de-4903-bb62-492bc9dd0a13)

The combination of all trained models put to use is located in Test.ipynb

## Baselines
The following trained models are included in Pretrained (Google collab):
- `Age_model_pretrained.h5'
- `mood_model_pretrained.h5'
- `gender_model_pretrained.h5'
