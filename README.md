# FakeProfileDetection-Transformers

## Overview

This repository contains the implementation of a Transformer-based model for detecting fake profiles on Instagram, combining **BERT** for text and metadata understanding, **Vision Transformer (ViT)** for visual analysis, and **Particle Swarm Optimization (PSO)** for hyperparameter optimization. The approach is evaluated on a combination of the **Cresci-2017 dataset** and a **custom-labeled Instagram dataset**, addressing both textual and visual content to enhance detection performance.

---

## Abstract

The increasing presence of fake profiles on Instagram raises significant concerns regarding user security, privacy, and the credibility of online interactions. To address these challenges, this study introduces a Transformer-based detection model integrating BERT and ViT architectures, optimized using the Particle Swarm Optimization (PSO) algorithm. The dataset includes attributes such as posting frequency, engagement metrics, follower-following ratio, bio-section characteristics, account age, linguistic patterns, and visual content from profile and post images. Preprocessing steps such as null value handling, feature scaling, and TF-IDF-based text transformation ensure data consistency and effective representation. BERT captures complex relationships in textual and metadata attributes, while ViT enhances visual feature extraction, with PSO optimizing hyperparameters like learning rate, attention heads, batch size, and image patch size. Experimental results show that the BERT-ViT-PSO model achieves a 96.4% accuracy, outperforming conventional deep learning classifiers with precision (95.9%), recall (97.1%), and F1-score (96.5%), highlighting the effectiveness of Transformer architectures and bio-inspired optimization techniques in strengthening security and authenticity on social media platforms.

---

## Dataset

The dataset used in this study includes:
- Cresci-2017 dataset (publicly available)
- A custom-labeled dataset of Instagram profiles

### Attributes:
- Textual: bio, captions, hashtags
- Visual: profile images, post banners
- Metadata: followers, following, post frequency, engagement ratio, account age, etc.

---

## Preprocessing

The preprocessing phase involved the following:

- **Null value handling** for missing metadata or image paths
- **Text preprocessing** including:
  - Lowercasing
  - Stopword removal
  - Emoji and URL stripping
  - Lemmatization
  - Tokenization
- **TF-IDF vectorization** applied to textual content for feature extraction
- **Min-Max normalization** of numerical attributes
- **Image preprocessing**: resizing (224×224), normalization, and patch generation for ViT

---

## Model Architecture

- **BERT**: For encoding textual and metadata features
- **ViT**: For processing profile and post images
- **PSO**: For optimizing hyperparameters including:
  - Learning rate
  - Batch size
  - Number of attention heads
  - Image patch size

---

## Requirements

```bash
python>=3.8  
transformers  
torch  
torchvision  
scikit-learn  
pandas  
numpy  
opencv-python  
matplotlib  
nltk  

