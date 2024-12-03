# Drug Name Detection using OCR

### Overview

This repository focuses on developing and evaluating Optical Character Recognition (OCR) pipelines for extracting drug names from images. The project leverages state-of-the-art OCR tools such as Tesseract and PaddleOCR (CRNN) to handle structured and unstructured text data effectively. Additionally, advanced preprocessing techniques and evaluation metrics are employed to improve performance.

Drug name detection from images is critical for applications in healthcare, pharmacy management, and supply chain monitoring. This project aims to:

- Extract drug names using OCR models.
- Improve the detection performance through preprocessing.
- Evaluate results using metrics like Fuzzy Similarity, Character Accuracy, and Word Error Rate (WER).

### Datast

The Drug Name Detection dataset contains 1823 images of pharmaceutical products sourced from various manufacturers and packaging styles. The dataset used for this project consists of images of drug packaging or labels. 

The images contain various pharmaceutical drug names, and the aim is to detect these names accurately.

The dataset includes images of medicine bottles, blister packs, vials, and other packaging formats commonly found in the healthcare industry. By using this dataset, researchers and practitioners can advance the development of accurate and efficient drug name detection systems, contributing to improved medication management and patient safety in the healthcare industry.

### Pipeline Description

##### Preprocessing:
- Grayscale conversion.
- Image resizing for clarity.
- Contrast enhancement using CLAHE.
- Noise reduction and sharpening.
- Binarization with Otsu's method.
- Rotation correction using Hough Transform.

 ##### OCR Models:
 - Tesseract OCR: Extracts text using a custom configuration.
        PaddleOCR (CRNN): Employs CRNN for robust text recognition.

##### Postprocessing:
- Fuzzy matching with a target drug name dictionary.
- Combination of Tesseract and PaddleOCR outputs.

##### Evaluation:
- Fuzzy Similarity Score.
- Character Accuracy.
- Word Error Rate (WER).

### Challenges Addressed

- Low-quality and noisy images.
- Skewed and rotated text.
- Small, overlapping, or multi-line text regions.
- Domain-specific fonts and terminology.

### Results

- Tesseract: Average Fuzzy Similarity (21%), Character Accuracy (Low on small and noisy text - 15.3%), Word Error Rate is high (3).1).
- PaddleOCR: Average Fuzzy Similarity (53%), Better handling of multi-line and rotated text - 89.4%), Word Error Rate is better (1.8).
- Combined Output: Average Fuzzy Similarity (58%), Higher handling of multi-line and rotated text - (92.4%), Word Error Rate improved (1.2).
  
### Future Work

- Fine-tune PaddleOCR with domain-specific data.
- Add a drug name dictionary for postprocessing.
- Improve preprocessing steps for noisy and skewed images.
- Implement ensemble methods for combining OCR outputs.

### Source

https://www.kaggle.com/datasets/pkdarabi/the-drug-name-detection-dataset
