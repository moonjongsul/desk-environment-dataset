# desk-environment-dataset
#### Desk environment data for __[Object detection]__, __[Segmentation]__, and __[Property estimation]__

### Dataset link: https://drive.google.com/drive/folders/1crN2H-TfBem6x4GYxcmqkuZDjUKmLTf0?usp=sharing

# The dataset is composed of 
### 13 classes of desk objects (RGBA images, background removed)
<img src="https://github.com/moonjongsul/desk-environment-dataset/blob/main/desk_objects.png" width="800" height="450">

### + 8 classes of cooking objects (RGBA images, background removed)
<img src="https://github.com/moonjongsul/desk-environment-dataset/blob/main/cooking_objects.png" width="800" height="300">

### + Object detection dataset and property estimation dataset (synthesized dataset using RGBA images)
**Object properties:** 
* The state of the object for the robot to manipulate the object
    - Object state (open region segment(open or close) -> gray scale)
* Contact region for the robot to manipulate object
    - Object contact region (heatmap -> gray scale)
* Manipulation type for robot to manipulate object
    - Object manipulation type (folding, sliding, screwing, ... -> class)
Document: https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9268261
<img src="https://github.com/moonjongsul/desk-environment-dataset/blob/main/detection.png" width="800" height="350">

* * *
# Data augmentation using background synthesis
1. Applying augmentation techniques to RGBA object image
2. Synthesize an augmented image to the background
<img src="https://github.com/moonjongsul/desk-environment-dataset/blob/todo/augmentation.jpg" width="800" height="190">

* * *
# Description of the dataset
## Structure
**desk_environment_dataset**
 * desk_objects
   * bin1
   * bin2
   * ...
   * objects_state
 * cooking_objects
   * apple
   * eggplant
   * ...
   * tongs
 * object_detection
   * cso5
     * Images
     * Labels
     * Masks
   * cso5_cocoform
     * train
     * train_annot
     * val
     * val_annot
 * state_estimation
   * cso5_aug     
     * train
     * test
     * cso5
       * train
       * test
 * semantic_segmentation
   * train
     * Annotations
     * images
     * labels
     * Masks
   * test    
     * Annotations
     * images
     * labels
     * Masks

## Files
```
objects: RGBA images and mask images of desk objects                     # for synthetic augmentation
object_detection: Synthesis images for object detection                  # for YOLO, EfficientDet, ... etc. 
property_estimation: Synthesis images for object property estimation     # for statenet
```
