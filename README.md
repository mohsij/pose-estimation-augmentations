# pose-estimation-augmentations
Augmentations used by team TangoUnchained in the Satellite Pose Estimation Competition 2021

## Usage
- Merge code in `object_detection` directory with detectron2 repo (https://github.com/facebookresearch/detectron2)
- Update the function `build_augmentation` in `detectron2/detectron2/data/detection_utils`
e.g you can add
    augmentation.extend([
        T.RandomRotation([0,45]),
        T.RandomTranslation([-100,100], [-100,100]),
   	)]
