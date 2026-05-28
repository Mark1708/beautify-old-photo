# beautify-old-photo

> Research notebook для восстановления деталей лиц и раскрашивания старых фотографий с помощью GFPGAN и DeOldify.

![Python](https://img.shields.io/badge/runtime-python%203-111827?style=for-the-badge&labelColor=111827&color=5b5ef4)
![Notebook](https://img.shields.io/badge/workflow-jupyter%20%2F%20colab-111827?style=for-the-badge&labelColor=111827&color=5b5ef4)
![Status](https://img.shields.io/badge/status-research%20snapshot-111827?style=for-the-badge&labelColor=111827&color=5b5ef4)

[English version](README.md)

| Поле | Значение |
|---|---|
| Статус | Исследовательский срез |
| Тип | ML-эксперимент / notebook-демо |
| Основной stack | Python 3, Jupyter / Google Colab, PyTorch, fastai, DeOldify, GFPGAN |
| Входные данные | Пользовательские фотографии в `/content/input` или локальные примеры в `assets/input/` |
| Ожидаемые результаты | Восстановленные лица, раскрашенные изображения и `colorized_output.zip` из workflow notebook |

## Цель

Репозиторий сохраняет экспериментальный notebook для улучшения старых или низкокачественных фотографий с минимальным ручным редактированием:

- восстановить лица перед раскрашиванием;
- раскрасить исходные и восстановленные изображения;
- сравнить локальные before/after examples.

Это исследовательское demo, а не production-сервис обработки изображений.

## Метод

Notebook объединяет два upstream-проекта:

- [GFPGAN](https://github.com/TencentARC/GFPGAN) для восстановления лиц на реальных фотографиях. В этом репозитории он загружается из внешнего Colab bundle, а не из `requirements.txt` и не из vendored source files.
- [DeOldify](https://github.com/jantic/DeOldify) для раскрашивания изображений. Upstream repository archived, поэтому проект стоит рассматривать как сохранённый срез, а не активно поддерживаемый pipeline.

Локальный `requirements.txt` содержит только top-level Python dependencies без pinned versions:

```txt
torch
fastai
deoldify
```

## Воспроизводимость

Самый реалистичный путь — открыть notebook в Google Colab и пройти его cells:

```sh
# опционально установить локальные зависимости для изучения notebook
pip install -r requirements.txt

# открыть notebook вручную
jupyter notebook BeautifyOldPhoto.ipynb
```

## Результаты

| До | После |
|---|---|
| <img src="assets/input/photo1.JPG" width="300" alt="Original old photo 1"> | <img src="assets/output/result_photo1.jpg" width="300" alt="Restored and colorized photo 1"> |
| <img src="assets/input/photo2.JPG" width="300" alt="Original old photo 2"> | <img src="assets/output/result_photo2.JPG" width="300" alt="Restored and colorized photo 2"> |

## Допущения и ограничения

- Лучше всего работает с фотографиями, где сохранились различимые детали лиц.
- Качество результата зависит от исходного разрешения, степени повреждения, model weights и runtime environment.
- Раскрашивание вероятностное и может добавлять исторически неточные цвета или визуальные артефакты.
- Workflow notebook зависит от external archives и upstream model files, поэтому он не полностью self-contained.
- Не загружайте чувствительные личные фотографии в сторонние notebook runtimes, если это не подходит вашим privacy requirements.
- Сгенерированные файлы могут сохранять image metadata в зависимости от processing path; проверяйте файлы перед публичной публикацией.

## Ссылки

- GFPGAN: <https://github.com/TencentARC/GFPGAN>
- DeOldify: <https://github.com/jantic/DeOldify>
- Notebook: [`BeautifyOldPhoto.ipynb`](BeautifyOldPhoto.ipynb)

## Статус

Исследовательский/учебный проект. Результаты, зависимости и runtime assumptions описаны для воспроизводимости, но репозиторий не поддерживается как packaged product.
