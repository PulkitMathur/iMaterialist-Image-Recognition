# iMaterialist-Image-Recognition

Goal: Automatic Product Recognition for Home Goods and Furniture Images

Challenge: Similarity in fine grained images and same picture could be taken at different angles, lighting, backgrounds and levels of occlusion.

Dataset:
  - Number of Classes: 128
  - Number of Training Images: 194,828
  - Number of Validation Images: 6,400
  - Number of Test Images: 12,800
  - Min images in a class: 332
  - Max images in a class: 3996
  
Model Architecture:
  - Each layer of the convnet has multiple convolution filters in parallel. 
  - Output from all filters are stacked up together.
  - The networks learns from low-level as well as high level features.  

Approach:
 - Training the model on Inception V-3:
   - With Random weights
   - With Pretrained Imagenet weights  
 - Perform grid search on hyperparameters

Next Steps:
  - Training Data Augmentation and on the fly training of the model.
  - Test Time Augmentation 
    - Average of the predictions Using random transforms of the image. 
  - Side-on/top-down transforms: angle and lighting + flipping about the horizontal and vertical axis and rotating by some angle theta.



