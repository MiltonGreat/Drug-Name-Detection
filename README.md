# Drug-Name-Detection

### Summary and Recommendations

#### 1. Overview

The goal of this project is to identify and extract the names of drugs from images, which can be useful in various fields like healthcare, pharmacy management, and supply chain monitoring. The project uses Tesseract OCR as the primary tool for extracting text from images. To improve the accuracy of the extraction, several preprocessing techniques like grayscale conversion, thresholding, and denoising have been applied.

#### 2. Datast

The Drug Name Detection dataset contains 1823 images of pharmaceutical products sourced from various manufacturers and packaging styles. The dataset used for this project consists of images of drug packaging or labels. The dataset is organized into different sets:

    train: for training
    test: for testing
    valid: for validation

The images contain various pharmaceutical drug names, and the aim is to detect these names accurately.

The dataset includes images of medicine bottles, blister packs, vials, and other packaging formats commonly found in the healthcare industry. By using this dataset, researchers and practitioners can advance the development of accurate and efficient drug name detection systems, contributing to improved medication management and patient safety in the healthcare industry.

#### 3. Interpretation

The results indicate that the OCR model struggled to accurately detect the drug names. This could be due to:

- Poor image quality
- Inadequate preprocessing
- Lack of domain-specific training (fine-tuning required for drug name detection)

#### 4. Next Steps and Improvements

Improving Preprocessing: Experiment with advanced noise reduction techniques, adaptive thresholding, and image rotation to correct misaligned or noisy images.

Custom Training or Fine-tuning: Fine-tune a model specifically for detecting drug names using the MobileNet SSD architecture or another lightweight model.

Post-Processing Heuristics: Implement dictionary lookups for common drug names to enhance the post-OCR results. Apply domain-specific rules for filtering and improving the accuracy of the detected names.

Optical Character Recognition (OCR): Try different OCR models or fine-tune Tesseract for better recognition performance in specific scenarios, such as drug name detection.

#### 5. Evaluation

This project uses WER (Word Error Rate) and character-level accuracy to better gauge the performance of the OCR model.

#### 6. Source

https://www.kaggle.com/datasets/pkdarabi/the-drug-name-detection-dataset
