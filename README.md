# Salt_detection_challenge
Image Segmentation project based on Kaggle's TGS salt detection competition.

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

More to be updated!
