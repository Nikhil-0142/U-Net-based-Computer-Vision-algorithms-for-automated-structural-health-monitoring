# U-Net-based-Computer-Vision-algorithms-for-automated-structural-health-monitoring


This repository represents the training and testing of the proposed U-net architectures for component and damage detection. the algorithms along with the requirements, dataset loading, testing and training scripts are given in the attached ipynb notebooks and can be opened in google colab below
- **Component recognition** : <a href="https://colab.research.google.com/github/Nikhil-0142/U-Net-based-Computer-Vision-algorithms-for-automated-structural-health-monitoring/blob/b9a2df0b7d4c02ed0c6cd8758af72ce6dc5216a1/U_Net_for_Component_Recognition(SHM).ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"></a>
- **Damage recognition** : <a href="https://colab.research.google.com/github/Nikhil-0142/U-Net-based-Computer-Vision-algorithms-for-automated-structural-health-monitoring/blob/4bc4b588dea24aabbcaaac24fb7e10fe802fe714/U_Net_for_Damage_Detection(SHM).ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"></a>


# Dataset
The U-net models for component and damage detections have been trained on the Tokaido dataset. The dataset is the property of Narazaki et.al.[1], and was published in their paper named "Synthetic environments for vision-based structural condition assessment of Japanese high-speed railway viaducts"

The dataset contains images created synthetically representing railway viaducts. The dataset has segmentation labels for various structural components like columns, beams, railway pylons etc in component recognition and has concrete cracks, and exposed rebears in damage detection. 

# Algorithms

## U-net for component detection
<img width="400" src="https://github.com/Nikhil-0142/U-Net-based-Computer-Vision-algorithms-for-automated-structural-health-monitoring/blob/fe9569777437548968bce93969e78c5796b7a6dc/data/unet.JPG"> </a>

## U-net for damage detection

<img width="400" src="https://github.com/Nikhil-0142/U-Net-based-Computer-Vision-algorithms-for-automated-structural-health-monitoring/blob/fe9569777437548968bce93969e78c5796b7a6dc/data/att_unet.JPG"> </a>

# Running the Notebooks

**The notebook is made and run in a Google Colab-Pro environment and will work best on similar or better computational resources.**

**The training data was saved on Google drive and hence our code is set up in a way that it imports the data from it, for any other cloud storage facility, necessary modifications will be required.**

## To train the model  

1) Firstly, run all the cells till the first checkpoint as they contain the necessary functions. 

2) To train the model, run the cells upto the second checkpoint, they contain the code for the data pipeline and importing the data from storage.

3) The dataset is imported using a text file containing absolute addresses of the images and labels which are stored in their respective directories.

4) The labels have to be one-hot-encoded which is done using the ‘get_label’ function.

5) Make necessary changes to the functions used for pre-processing in accordance with the dataset format you’re using.

6) Cells after the second checkpoint contain the model definitions and the parts and building blocks of the model. Run them to create the model.

7) Then, from the third checkpoint onward, cells have the definitions of metrics, optimizer, loss function, checkpoint callback to save the model weights, and finally the model compilation.

8) The next cell contains the code to load the trained weights from the saved checkpoints, run if applicable.

9) Run the next cell to start the training by setting the number of epochs as required.

10) The next set of cells, till checkpoint five, contain the code to print the model training history to see how the training metrics changed wrt each epoch, and then print out the predictions on the validation set.

## To test the model

1) Run the training steps 1,3,4 and 5. The model will be loaded and ready for predictions. 

2) Go to checkpoint 5 and run the cells following that, they contain the code to import the test dataset and create a tf.data pipeline for the same.

3) After importing the dataset, running the following cells will print the results. 

4) The cells from checkpoints 6 to 7 contain the code to upscale the model output (192x320) to the required size (360x640).

The last cell contains the code to upscale the images if the desired image size of the output is different.
The image size used in the model has been decreased for faster training and reduced memory usage and can be increased in case resources permit.


# Component detection

## Validation Image Inference

<img width="600" src="https://github.com/Nikhil-0142/U-Net-based-Computer-Vision-algorithms-for-automated-structural-health-monitoring/blob/fe9569777437548968bce93969e78c5796b7a6dc/data/Component_valid.JPG"> </a>

## Test Image Inference

<img width="600" src="https://github.com/Nikhil-0142/U-Net-based-Computer-Vision-algorithms-for-automated-structural-health-monitoring/blob/fe9569777437548968bce93969e78c5796b7a6dc/data/Component_test.JPG"> </a>

# Damage detection

## Validation Image Inference

<img width="600" src="https://github.com/Nikhil-0142/U-Net-based-Computer-Vision-algorithms-for-automated-structural-health-monitoring/blob/fe9569777437548968bce93969e78c5796b7a6dc/data/crack_valid.JPG"> </a>

## Test Image Inference

<img width="600" src="https://github.com/Nikhil-0142/U-Net-based-Computer-Vision-algorithms-for-automated-structural-health-monitoring/blob/fe9569777437548968bce93969e78c5796b7a6dc/data/Crack_test.JPG"> </a>

# Reference
1) Narazaki, Yasutaka & Hoskere, Vedhus & Yoshida, Koji & Spencer, Billie & Fujino, Yozo. (2021). Synthetic environments for vision-based structural condition assessment of Japanese high-speed railway viaducts. Mechanical Systems and Signal Processing. 160. 107850. 10.1016/j.ymssp.2021.107850. 
