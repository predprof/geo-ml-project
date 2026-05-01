# Выявление зон деградации растительного покрова

Проект по анализу спутниковых изображений Landsat для выявления зон деградации растительности.

## Установка зависимостей

```bash
pip install -r requirements.txt
```

## Опциональная установка PyTorch для U-Net

Если вы хотите использовать секцию Deep Learning (U-Net), установите PyTorch:

**macOS/Linux:**
```bash
pip install torch torchvision
```

**Windows:**
```bash
pip install torch torchvision --index-url https://download.pytorch.org/whl/cpu
```

**С GPU (CUDA):**
```bash
pip install torch torchvision --index-url https://download.pytorch.org/whl/cu118
```

## Структура проекта

- `project_clean.ipynb` - основной notebook с полной реализацией
- `landsat_data/` - папка с локальными снимками Landsat
- `LANDSAT_DOWNLOAD_GUIDE.md` - инструкция по скачиванию данных
- `requirements.txt` - список зависимостей

## Методы, используемые в проекте

### Классические методы
- Пороговая классификация по ΔNDVI

### Supervised Learning
- Random Forest
- SVM (Support Vector Machine)
- Gradient Boosting

### Unsupervised Learning
- K-means кластеризация
- DBSCAN кластеризация

### Deep Learning
- U-Net для семантической сегментации (требует PyTorch)

## Запуск

1. Скачайте данные Landsat согласно `LANDSAT_DOWNLOAD_GUIDE.md`
2. Разместите их в папке `landsat_data/`
3. Откройте `project_clean.ipynb` в Jupyter
4. Запустите все ячейки

## Примечание

Секция U-Net автоматически пропускается, если PyTorch не установлен. Все остальные методы работают без PyTorch.
