# desk-environment-dataset
#### Desk environment data for __[Object detection]__, __[Segmentation]__, and __[State estimation]__

### Dataset link: https://drive.google.com/drive/folders/1crN2H-TfBem6x4GYxcmqkuZDjUKmLTf0?usp=sharing

# The dataset is composed of 
### 13 classes of desk objects (RGBA images, background removed)
<img src="https://github.com/moonjongsul/desk-environment-dataset/blob/main/desk_objects.png" width="800" height="450">

### + 8 classes of cooking objects (RGBA images, background removed)
<img src="https://github.com/moonjongsul/desk-environment-dataset/blob/main/cooking_objects.png" width="800" height="300">

### + Object detection dataset and state estimation dataset (synthesized dataset using RGBA images)
<img src="https://github.com/moonjongsul/desk-environment-dataset/blob/main/detection.png" width="800" height="350">

### Object state data
This is a data set for estimating the state and properties of an object.
This data consists of four types.
- Object image (single image -> RGB scale)
- Object manipulation type (folding, sliding, screwing, ... -> class)
- Object contact region (heatmap -> gray scale)
- Object state (open region segment(open or close) -> gray scale)

* * *
# Data augmentation using background synthesis
(source code is not included in this repo)
1. Applying augmentation techniques to RGBA object image
2. Synthesize an augmented image to the background
<img src="https://github.com/moonjongsul/desk-environment-dataset/blob/todo/augmentation.jpg" width="800" height="190">

* * *
# Description of the dataset
## Structure
```
desk_environment_dataset
 ㄴ desk_objects
    ㄴ bin1
    ㄴ bin2
    ...
    ㄴ objects_state
 ㄴ cooking_objects
    ㄴ apple
    ㄴ eggplant
    ...
    ㄴ tongs
 ㄴ object_detection
    ㄴ cso5
       ㄴ Images
       ㄴ Labels
       ㄴ Masks
    ㄴ cso5_cocoform
       ㄴ train
       ㄴ train_annot
       ㄴ val
       ㄴ val_annot
 ㄴ state_estimation
    ㄴ cso5_aug     
       ㄴ train
       ㄴ test
    ㄴ cso5
       ㄴ train
       ㄴ test
 ㄴ semantic_segmentation
    ㄴ train
       ㄴ Annotations
       ㄴ images
       ㄴ labels
       ㄴ Masks
    ㄴ test    
       ㄴ Annotations
       ㄴ images
       ㄴ labels
       ㄴ Masks
```

## Files
```
objects: RGBA images and mask images of desk objects               # for synthetic augmentation
object_detection: Synthesis images for object detection            # for YOLO, EfficientDet, ... etc. 
state_estimation: Synthesis images for object state estimation     # for statenet
```
