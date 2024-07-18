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
│       ├── Dataset
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
│   ├── Keras-OCR
│   │   ├── Code
│   │   ├── Model
│   │   └── requirements.txt
│   └── YOLO-OCR
│       ├── README.md
│       ├── YOLO
│       ├── requirements.txt
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
python src/Keras-OCR/Code/predictions.py -m models/keras-recognizer_custom.h5 -i data/raw/test -o data/interim/cleaned -j data/processed/predictions
```

### Training the CRNN Model

To train the CRNN text recognizer, use the following command:
```bash
python src/YOLO-OCR/src/train-crnn.py --dataset data/raw/train --labels data/raw/train/labels.txt --model models/crnn_model.h5 --epochs 50 --batch_size 32
```
Replace the paths with your actual dataset and labels paths.

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

By following these steps, you should be able to integrate and run the scripts from `DeepLearningSpanishAmerican-master` within your `handwriting_recognition_project`. Ensure paths are correctly set and dependencies are installed properly.
```