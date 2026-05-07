# Dataset Documentation

## Data Sources
This project utilizes a combination of two primary datasets to ensure a diverse range of clinical mange and scabies presentations:

* **Dog Skin Diseases (Kaggle):** Used for Demodicosis and Healthy skin categories. [View Dataset](https://www.kaggle.com/datasets/youssefmohmmed/dogs-skin-diseases-image-dataset)
* **Skin Disease Raw Dataset (Kaggle):** Used specifically to source human Scabies cases. [View Dataset](https://www.kaggle.com/datasets/devdope/skin-disease-raw-dataset)

## Preprocessing
Raw images were filtered to isolate the three target classes and resized to **640x640** pixels to ensure compatibility with the YOLOv8 Nano architecture.
