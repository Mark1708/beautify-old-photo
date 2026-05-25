# beautify-old-photo

Research / ML demo для восстановления и раскрашивания старых фотографий.

[English version](README.md)

## Мотивация

Notebook исследует, как современные image restoration модели могут улучшать старые или низкокачественные фотографии с минимальным ручным редактированием.

## Метод

- GFPGAN для восстановления лиц
- DeOldify для colorization
- Jupyter Notebook / Google Colab workflow

## Результаты

| Before | After |
|---|---|
| <img src="https://github.com/Mark1708/beautify-old-photo/raw/main/assets/input/photo1.JPG" width="300"> | <img src="https://github.com/Mark1708/beautify-old-photo/raw/main/assets/output/result_photo1.jpg" width="300"> |
| <img src="https://github.com/Mark1708/beautify-old-photo/raw/main/assets/input/photo2.JPG" width="300"> | <img src="https://github.com/Mark1708/beautify-old-photo/raw/main/assets/output/result_photo2.JPG" width="300"> |

## Ограничения

- Лучше всего работает с фотографиями, где сохранились различимые детали лиц.
- Качество результата зависит от исходного разрешения и степени повреждения фотографии.
- Colorization вероятностная, поэтому возможны артефакты.
- Это experiment, а не production image-processing pipeline.

## Воспроизводимость

1. Установить зависимости из `requirements.txt`.
2. Открыть `BeautifyOldPhoto.ipynb` в Jupyter или Google Colab.
3. Следовать notebook cells для подключения или подготовки input images.

## Credits

- GFPGAN: https://github.com/TencentARC/GFPGAN
- DeOldify: https://github.com/jantic/DeOldify

## Статус

Research demo only.
