# Multimodal Recommendation System
** This file is a bit huge please download it to view it fully!! **
This repository contains the implementation of a Multimodal Recommendation System, leveraging text and image embeddings to provide product recommendations. The system integrates natural language processing (NLP) and computer vision (CV) models to create a robust solution for e-commerce applications.

---
## Overview
This project implements a recommendation system combining:

- **Text embeddings**: Capturing semantic information from product descriptions using `SentenceTransformer`.
- **Image embeddings**: Extracting visual features from product images using a `ResNet50` architecture.

These embeddings are concatenated to create a multimodal feature vector, enabling similarity-based recommendations.

---

## Dataset
The dataset includes:

- **Metadata**: A CSV file with product descriptions and attributes.
- **Images**: Product images stored in a directory.

### Example Metadata Fields:
- `id`: Unique product identifier.
- `productDisplayName`: Text description of the product.
- `articleType`: Product category.

---

## Preprocessing

## Text Data:
- Encode categorical variables using `LabelEncoder`.
- Generate TF-IDF vectors for product descriptions.

## Image Data:
- Load images using `PIL`.
- Resize images to `224x224` for ResNet50 input.

## Splitting Data:
- Split into training and testing sets using `train_test_split`.

---

## Model Architecture

## Text Embeddings:
- `SentenceTransformer` (model: `stsb-distilbert-base`) encodes product descriptions into 128-dimensional vectors.

## Image Embeddings:
- `ResNet50` extracts features from images, averaged to generate a fixed-length vector.

## Feature Concatenation:
- Text and image embeddings are concatenated and normaliz

## Results
 - Example Recommendations:
 - Input Product: Original product image and description.
 - Output: Top 5 similar products based on multimodal embeddings.
## Requirements

### Libraries
- Python 3.x
- TensorFlow
- PyTorch
- scikit-learn
- Matplotlib
- PIL
- SentenceTransformer
- Transformers
- NLTK


