# desk-environment-dataset
#### Desk environment data for __[Objects images]__, __[Object detection]__, and __[State estimation]__

## The dataset is composed of 
### 13 classes of desk objects (RGBA images)
<img src="https://github.com/moonjongsul/desk-environment-dataset/blob/main/desk_objects.png" width="800" height="450">

### + 8 classes of cooking objects (RGBA images)
<img src="https://github.com/moonjongsul/desk-environment-dataset/blob/main/cooking_objects.png" width="800" height="300">

### + Object detection dataset and state estimation dataset (synthesized dataset)
<img src="https://github.com/moonjongsul/desk-environment-dataset/blob/main/detection.png" width="800" height="350">

### Dataset link: https://koreaoffice-my.sharepoint.com/:f:/g/personal/jhj0630_korea_edu/ErxsMxdoIaZHm9dlnVPQTlwB_Jo4VxIYvxA3Jw7nFL8F2g?e=jlA0uZ

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
