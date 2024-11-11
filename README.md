# Drug-Name-Detection

### Summary and Recommendations

#### 1. Overview

The goal of this project is to identify and extract the names of drugs from prescription labels and other images using Optical Character Recognition (OCR) techniques. The project uses various OCR models, such as Tesseract, PaddleOCR (CRNN), and custom image preprocessing methods, to process images and improve text extraction accuracy.

#### 2. Datast

The Drug Name Detection dataset contains 1823 images of pharmaceutical products sourced from various manufacturers and packaging styles. The dataset used for this project consists of images of drug packaging or labels. The dataset is organized into different sets:

    train: for training
    test: for testing
    valid: for validation

The images contain various pharmaceutical drug names, and the aim is to detect these names accurately.

The dataset includes images of medicine bottles, blister packs, vials, and other packaging formats commonly found in the healthcare industry. By using this dataset, researchers and practitioners can advance the development of accurate and efficient drug name detection systems, contributing to improved medication management and patient safety in the healthcare industry.

#### 3. Image Preprocessing and OCR

The preprocess_image function applies multiple preprocessing steps to improve the image quality for OCR. The preprocessing steps include:

- Grayscale conversion
- Image resizing
- Gaussian blur for noise reduction
- Sharpening using a Laplacian filter
- Contrast enhancement with CLAHE
- Binarization using Otsu’s thresholding
- Rotation correction using Hough Line Transform

#### 4. Evaluation

The project evaluates OCR models using the following metrics:

    Fuzzy Similarity: Measures the similarity between the extracted text and the target text using fuzzy string matching.
    Character Accuracy: Measures the accuracy of the characters in the extracted text compared to the target text.
    Word Error Rate (WER): A metric used to compare the error rate in the words extracted by OCR models.

#### 5. Source

https://www.kaggle.com/datasets/pkdarabi/the-drug-name-detection-dataset
