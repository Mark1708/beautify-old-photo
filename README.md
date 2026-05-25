# beautify-old-photo

Research and ML demo for restoring and colorizing old photos.

[Русская версия](README.ru.md)

## Motivation

This notebook explores how modern image restoration models can improve aged or low-quality photos with minimal manual editing.

## Method

- GFPGAN for face restoration
- DeOldify for colorization
- Jupyter Notebook / Google Colab workflow

## Results

| Before | After |
|---|---|
| <img src="https://github.com/Mark1708/beautify-old-photo/raw/main/assets/input/photo1.JPG" width="300"> | <img src="https://github.com/Mark1708/beautify-old-photo/raw/main/assets/output/result_photo1.jpg" width="300"> |
| <img src="https://github.com/Mark1708/beautify-old-photo/raw/main/assets/input/photo2.JPG" width="300"> | <img src="https://github.com/Mark1708/beautify-old-photo/raw/main/assets/output/result_photo2.JPG" width="300"> |

## Limitations

- Works best on photos with recoverable facial detail.
- Output quality depends on source resolution and damage level.
- Colorization is probabilistic, so some artifacts are expected.
- This is an experiment, not a production image-processing pipeline.

## Reproducibility

1. Install dependencies from `requirements.txt`.
2. Open `BeautifyOldPhoto.ipynb` in Jupyter or Google Colab.
3. Follow the notebook cells to mount or prepare input images.

## Credits

- GFPGAN: https://github.com/TencentARC/GFPGAN
- DeOldify: https://github.com/jantic/DeOldify

## Status

Research demo only.
