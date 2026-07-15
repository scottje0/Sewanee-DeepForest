# Sewanee-DeepForest
DeepForest is an object detection model developed to identify and classify objects from airborne RGB imagery. This project locally trains a model of DeepForest to be used on the Domain of the University of the South (Sewanee). In this project, we customized two different models of DeepForest: an object detector capable of identifying individual tree crowns, and a species detection model capable of classifying some of the tree species present across the domain. 

## The Training Process
For the object detection model, we loaded the pre-trained tree crown detection model from DeepForest. To further modify the model, we used ten randomly selected 20x20 meter plots and ten additional plots of various sizes from two different forests on the domain. We labeled each individual tree crown in Label Studio and exported those annotations to DeepForest to train the model. 

For the species detection model, we used the DeepForest CropModel and trained it on 13 species classes found in the ten 20x20 meter plots. This includes chestnut oak, white oak, black oak, scarlet oak, mockernut hickory, pale hickory, pignut hickory, tulip poplar, sourwood, sassafras, sugar maple, red maple, and dead. We used a similar method to training the object detector: labeling each species class in Label Studio, exporting the annotations to DeepForest, and training the model. 

## Contents
This page contains the scripts and data required to accurately reproduce our DeepForest models for their future use and continual training. There is much room for improvement on these models, as their accuracy statistics are still in the preliminary phase of training, but this serves as baseline training for continual reproductions and additions. 

## Citations
Weinstein, B.G., Marconi, S., Aubry‐Kientz, M., Vincent, G., Senyondo, H. and White, E.P., 2020. DeepForest: A Python package for RGB deep learning tree crown delineation. Methods in Ecology and Evolution, 11(12), pp.1743-1751. https://doi.org/10.1111/2041-210X.13472 

Weinstein, B.G.; Marconi, S.; Bohlman, S.; Zare, A.; White, E.P., 2019. Individual Tree-Crown Detection in RGB Imagery Using Semi-Supervised Deep Learning Neural Networks. Remote Sensing 11, 1309 https://doi.org/10.3390/rs11111309
