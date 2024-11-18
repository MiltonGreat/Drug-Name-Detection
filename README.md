# Drug-Name-Detection

### Overview

This project uses the Drug Name Detection dataset from Kaggle, which includes 1,823 images of pharmaceutical product labels from various manufacturers and packaging styles. The goal is to develop and evaluate Optical Character Recognition (OCR) models for accurately identifying drug names from complex and noisy label images.

The dataset includes a diverse range of packaging formats (e.g., medicine bottles, blister packs, vials) and text styles, making it ideal for training and testing OCR pipelines for healthcare applications such as drug name verification, label digitization, and automated inventory management.

### Datast

The Drug Name Detection dataset contains 1823 images of pharmaceutical products sourced from various manufacturers and packaging styles. The dataset used for this project consists of images of drug packaging or labels. 

The images contain various pharmaceutical drug names, and the aim is to detect these names accurately.

The dataset includes images of medicine bottles, blister packs, vials, and other packaging formats commonly found in the healthcare industry. By using this dataset, researchers and practitioners can advance the development of accurate and efficient drug name detection systems, contributing to improved medication management and patient safety in the healthcare industry.

### Image Preprocessing and OCR

The preprocess_image function applies multiple preprocessing steps to improve the image quality for OCR. The preprocessing steps include:

- Grayscale conversion
- Image resizing
- Gaussian blur for noise reduction
- Sharpening using a Laplacian filter
- Contrast enhancement with CLAHE
- Binarization using Otsu’s thresholding
- Rotation correction using Hough Line Transform

### Challenges Addressed

- Low-quality and noisy images.
- Skewed and rotated text.
- Small, overlapping, or multi-line text regions.
- Domain-specific fonts and terminology.

### Results

- Tesseract: Average Fuzzy Similarity (~25%), Character Accuracy (Low on small and noisy text).
- PaddleOCR: Average Fuzzy Similarity (~30%), Better handling of multi-line and rotated text.

### Future Work

- Fine-tune OCR models with domain-specific data.
- Train custom recognition models (e.g., CRNN, Transformer-based).
- Add noise, blur, and distortions to simulate real-world conditions.
- Build a GUI or deploy as a web app for real-time drug label detection.

### Source

https://www.kaggle.com/datasets/pkdarabi/the-drug-name-detection-dataset
