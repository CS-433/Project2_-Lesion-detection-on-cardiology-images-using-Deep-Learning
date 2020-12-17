# Project2_EPH_Lesion_localization
This project is about culprit lesion localization on cardiology images.

## Data access

The data we used are available on this link: https://drive.switch.ch/index.php/s/367fkbeytfy24d8/authenticate but first you have to ask for access to dorina.thanou@epfl.ch.
Although you can use different images, it's up to you, a folder 'data' must be created and it will contained all other folders of the images mentionned below.
When such directory is used '/home/raes/Project2' it's up to you to change it to your own directory.
## How to run 

We have two diffrenrent CNN implementations:
  
  # UNET
  The first one is a Unet, in the folder: "UNET_FINAL.ipynb"
  The data has to be put in two folders, "raw" with the raw images and "labelled" with red and green dot on the culprit regions.
  The augmented images have to be put into the corresponding folders previously created (check the code to see the needed folders).
  
  The first part of the code is dedicated to the targets creation.
  After threshold selection of the culprit region, a clustering algorithms is used to create target with only one culprit regions.

  Then the Unet architecture is implemented and the training of the model. You can run each cell one by one to train the Unet and display the results, even if you 
  have no access to a GPU you can try to launch it but it will likely not work.
  
  # Regression CNN
  The second one is a CNN regresion, in the folder: "Regression_NN.ipynb"
  The code structure is similar to the Unet implementation but the target is composed of (x,y), the culprit region center coordinates, that are loaded in the first cells.
  Be careful to create 'xy_inputs' folder in 'data/' and also to set the directory on this 'data/' folder for saving 'targets_xy' pickle file.
  
  Once again you can launch each cell one by one and check the commentary to change the trainng part.
  
