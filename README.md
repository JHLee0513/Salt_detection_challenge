# Salt_detection_challenge
Image Segmentation project based on Kaggle's TGS salt detection competition.

# What is this competition about? 
"Several areas of Earth with large accumulations of oil and gas also have huge deposits of salt below the surface.
But unfortunately, knowing where large salt deposits are precisely is very difficult. Professional seismic imaging still requires expert human interpretation of salt bodies. This leads to very subjective, highly variable renderings. More alarmingly, it leads to potentially dangerous situations for oil and gas company drillers." - from competition description.

In this competition TGS provided images collected using seismic reflection of the ground in various locations. Thus in the data we are given training data as the images and their appropriate masks highlighting the salt deposit within that image as labels. The goal of the competition is to build a model that best performs this image segmentation task.

# Major ideas implemented in this project:
* Image segmentation model using U-net architecture UpSampling layers in Keras
* ResNet50 as encoder model of the segmentation model
* Image augmentation using opencv and numpy
* Test Time Augmentation (TTA) to predict stronger predictions
* Stratified K-Fold ensembling to develop a better-generalizing model
* Experimented with vanilla U-Net, SGD and Adam optimizers, BCE, DICE, lovas-hinge loss functions
* Experimented with flip, padding, crop augmentations
* Experimented with horizontal flip TTA

# Performance & final results:
* Final model - ResNet50 encoder with squeeze and excitation modules with U-Net architecture
* Upsampling layers used instead of transpose concatenating Conv layers
* Adam optimizer
* Cosine annealing with model checkpoints
* Binary Cross Entropy (BCE) with DICE loss as loss function
* Submission: 0.807 Public LeaderBoard score

# Background knowledge & furhter explanation of ideas discussed in this notebook:


More to be updated!
