# Drug Name Detection using OCR

### Overview

A Python-based Optical Character Recognition (OCR) system specifically designed for extracting drug names from images. This project combines traditional OCR techniques with YOLO-based text detection and includes preprocessing steps optimized for pharmaceutical packaging.
Drug name detection from images is critical for applications in healthcare, pharmacy management, and supply chain monitoring. 

### Datast

The Drug Name Detection dataset contains 1823 images of pharmaceutical products sourced from various manufacturers and packaging styles. The dataset used for this project consists of images of drug packaging or labels. 

The images contain various pharmaceutical drug names, and the aim is to detect these names accurately.

The dataset includes images of medicine bottles, blister packs, vials, and other packaging formats commonly found in the healthcare industry. By using this dataset, researchers and practitioners can advance the development of accurate and efficient drug name detection systems, contributing to improved medication management and patient safety in the healthcare industry.

### Pipeline Description

1. Preprocessing
- Grayscale conversion
- Gaussian blur for noise reduction
- Otsu's thresholding
- Morphological operations

2. Text Detection
- YOLOv8 model for text region detection
- Bounding box extraction

3. OCR Processing
- Tesseract OCR with custom configuration
- Drug name extraction
- Text cleaning and normalization

4. Post-processing
- Special character removal
- Common OCR error correction
- Drug name validation

### Evaluation
The system includes evaluation metrics using:

Accuracy scoring
Fuzzy string matching
Custom drug name comparison logic

### Challenges Addressed

- Low-quality and noisy images.
- Skewed and rotated text.
- Small, overlapping, or multi-line text regions.
- Domain-specific fonts and terminology.

### Results

- Tesseract: Average Fuzzy Similarity (21%), Character Accuracy (Low on small and noisy text - 15.3%), Word Error Rate is high (3).1).
- PaddleOCR: Average Fuzzy Similarity (53%), Better handling of multi-line and rotated text - 89.4%), Word Error Rate is high (1.8).
- Combined Output: Average Fuzzy Similarity (58%), Higher handling of multi-line and rotated text - (92.4%), Word Error Rate is high (1.2).
- High word error rate indicatesg that the model struggles to accurately transcribe the text.
  
### Future Work

- Fine-tune PaddleOCR with domain-specific data.
- Add a drug name dictionary for postprocessing.
- Improve preprocessing steps for noisy and skewed images.
- Implement ensemble methods for combining OCR outputs.

### Source

https://www.kaggle.com/datasets/pkdarabi/the-drug-name-detection-dataset
