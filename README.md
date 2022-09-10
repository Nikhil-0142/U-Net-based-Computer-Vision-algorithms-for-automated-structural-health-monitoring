# U-Net-based-Computer-Vision-algorithms-for-automated-structural-health-monitoring
End-to-end implementation of U-Net based computer vision algorithms for automated structural health monitoring of reinforced concrete structures.

this repository represents the training and testing of the proposed U-net architectures for componennt and demage detection. the algorithms along with the requirements, dataset loading, testing and training scripts are given in the attached ipynb notebooks and can be opened in google colab below

- **Component recognition** : <a href="https://colab.research.google.com/github/RajaFida/YOLO-V5-Road-distress-imaging/blob/main/Test_YoloV5.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"></a>
- **Damage recognition** : <a href="https://colab.research.google.com/github/RajaFida/YOLO-V5-Road-distress-imaging/blob/main/Test_YoloV5.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"></a>


# Dataset
U-net models for component detection and damage detection were trained on Tokaido dataset, which has been developedd by Narazaki et.al., and was published in their paper named ;;
the dataset contains synthetic images of tokaido railway viaducts, and has segementation labebls for varioous structural components like columns, beams, railway pylons etc in component recognition, and concrete cracks, exposed rebears in demage detection. 

# Algorithms

## U-net for component detection
<img width="400" src="https://github.com/RajaFida/U-Net-based-Computer-Vision-algorithms-for-automated-structural-health-monitoring/data/unet.JPG"> </a>
