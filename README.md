```markdown
# Handwriting Recognition Project

This project aims to recognize handwritten text using deep learning models. It integrates resources from the [DeepLearningSpanishAmerican-master](https://github.com/username/DeepLearningSpanishAmerican-master) repository.

## Project Structure

```
handwriting_recognition_project
├── LICENSE
├── Makefile
├── README.md
├── data
│   ├── external
│   ├── interim
│   ├── processed
│   └── raw
│       ├── CharactersDataset
│       │   ├── TestSet
│       │   └── TrainingSet
│       ├── Dataset
│       │   ├── Test
│       │   └── Training
│       ├── test
│       ├── train
│       └── validation
├── docs
├── models
│   ├── InceptionResnet.py
│   ├── inceptionv3.py
│   ├── nasnet.py
│   └── vgg16.py
├── notebooks
├── reports
│   └── figures
├── requirements.txt
├── setup.cfg
├── src
│   ├── __init__.py
│   ├── config.py
│   ├── dataset.py
│   ├── features.py
│   ├── modeling
│   │   ├── __init__.py
│   │   ├── predict.py
│   │   └── train.py
│   ├── visualization
│   │   └── plots.py
│   ├── Keras-OCR
│   │   ├── Code
│   │   │   ├── IoU.py
│   │   │   ├── cleanImage.py
│   │   │   ├── kg.py
│   │   │   └── predictions.py
│   │   ├── Model
│   │   │   └── keras-recognizer_custom.h5
│   │   └── requirements.txt
│   └── YOLO-OCR
│       ├── README.md
│       ├── YOLO
│       │   └── words
│       └── src
│           ├── predict-crnn.py
│           ├── predict-yolo-ocr.py
│           ├── predict-yolo.py
│           ├── save-words.py
│           └── train-crnn.py
└── scripts
```

## Installation

1. Clone the repository:
```bash
git clone https://github.com/isabelklint/handwriting_recognition_project.git
cd handwriting_recognition_project
```

2. Create and activate a virtual environment:
```bash
python -m venv env
source env/bin/activate
```

3. Install the dependencies:
```bash
pip install -r requirements.txt
```

## Usage

### Running the Keras-OCR Predictions

To run the Keras-OCR predictions, use the following command:
```bash
python src/Keras-OCR/Code/predictions.py -m <model_path> -i <images_path> -o <output_path> -j <json_path>
```

- `model_path`: Path to the Keras-OCR model weights (e.g., `models/keras-recognizer_custom.h5`)
- `images_path`: Path to the directory containing input images (e.g., `data/raw/test`)
- `output_path`: Path to the directory where cleaned images will be saved (e.g., `data/interim/cleaned`)
- `json_path`: Path to the directory where output JSON files will be saved (e.g., `data/processed/predictions`)

### Running the YOLO-OCR Predictions

To run the YOLO-OCR predictions, use the following command:
```bash
python src/YOLO-OCR/src/predict-yolo-ocr.py
```

## Directory Structure

- `data/raw`: Contains raw data, including training, testing, and validation datasets.
- `models`: Contains the deep learning models.
- `src/Keras-OCR`: Contains the Keras-OCR scripts and models.
- `src/YOLO-OCR`: Contains the YOLO-OCR scripts and models.
- `notebooks`: Contains Jupyter notebooks for data exploration and analysis.
- `reports`: Contains generated reports and figures.
- `docs`: Contains project documentation.

## Contributing

We welcome contributions! Please see the contributing guidelines for more information.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.
```

This provides a clear overview of the project, its structure, and how to run the scripts and models.