# Augmentations by Team TangoUnchained

## Contents
This repo contains code for the following augmentations used by team TangoUnchained in the Satellite Pose Estimation Competition 2021.
Some of these augmentations were effective in producing the final model and are mentioned in the competition results paper cited below

Objection Detection augmentations:
```
RandomTranslation
RandomNoise
RandomStars
RandomHaze
RandomFlares
RandomStreaks
RandomBloom
RandomErasing
```

Landmark Regression augmentations:
(Will be uploaded soon)

## Usage
- Merge code in `object_detection` directory with detectron2 repo (https://github.com/facebookresearch/detectron2)
- Update the function `build_augmentation` in `detectron2/detectron2/data/detection_utils`
e.g you can add
```
augmentation.extend([
    T.RandomRotation([0,45]),
    T.RandomTranslation([-100,100], [-100,100]),
)]
```

## Citation

Please cite the following paper if you use this code:

```
@article{park2023satellite,
  title={Satellite Pose Estimation Competition 2021: Results and analyses},
  author={Park, Tae Ha and M{\"a}rtens, Marcus and Jawaid, Mohsi and Wang, Zi and Chen, Bo and Chin, Tat-Jun and Izzo, Dario and D’Amico, Simone},
  journal={Acta Astronautica},
  year={2023},
  publisher={Elsevier}
}
```
