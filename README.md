# FakeProfileDetection-Transformers

## 1. Project Title  
**FakeProfileDetection-Transformers**: A Multimodal Transformer-Based Framework for Detecting Fake Instagram Profiles Using BERT, ViT, and PSO Optimization.

---

## 2. Description  

This project implements an advanced deep learning pipeline to detect fake profiles on Instagram by leveraging both textual and visual content. The framework employs **BERT** for understanding profile bios, captions, and metadata, and **Vision Transformer (ViT)** for extracting features from profile images and post visuals. A **Particle Swarm Optimization (PSO)** algorithm is used to fine-tune hyperparameters for optimal performance. The model is evaluated on a hybrid dataset comprising the public **Cresci-2017 dataset** and a custom-labeled Instagram dataset.

---

## 3. Dataset Information  

### Sources:
- **Cresci-2017 Dataset** (Publicly available bot detection dataset): The Cresci-2017 Dataset is a publicly available and widely used benchmark dataset for social bot detection on Twitter. It was introduced by Stefano Cresci et al. in their 2017 research paper titled “The Paradigm-Shift of Social Spambots: Evidence, Theories, and Tools for the Arms Race”. This dataset is notable for its high-quality labeling and for capturing various types of automated and genuine Twitter behavior, making it a valuable resource for evaluating bot detection algorithms and studying online disinformation.

- The **Cresci-2017 dataset** comprises five Twitter user classes, each representing distinct behavior profiles:

- **Genuine Accounts**  
  Real Twitter users manually collected and verified.  
  Reflect natural human behavior such as varying tweet times, diverse content, and typical interactions.

- **Social Spambots #1, #2, and #3**  
  These are automated accounts designed to mimic real users while promoting content or manipulating online discourse.  
  The three subgroups represent increasing levels of sophistication, from basic automation to more advanced evasion techniques (e.g., behavioral camouflage and content variability).

- **Traditional Spambots**  
  Classic spam accounts exhibiting overt bot-like behavior such as excessive posting, repetitive content, and suspicious URLs.

- **Custom Instagram Dataset** (Manually labeled with genuine and fake profiles)

### Key Attributes:
- **Textual**: Biography text, post captions, hashtags  
- **Visual**: Profile images, post banners  
- **Metadata**:  
  - Number of followers/following  
  - Follower-following ratio  
  - Posting frequency and engagement metrics  
  - Account creation date and activity patterns  

*Note: Due to privacy concerns, the custom dataset is not publicly released in this repository. Contact the author for academic use.*

---

## 4. Code Information  

This repository contains the following components:
- `Fake_Accounts/users.csv`: CSV file containing fake user profile data  
- `Genuine_Accounts/users.csv`: CSV file containing genuine user profile data  
- `bert_vit_ready_10k.csv`: Combined, preprocessed dataset ready for model input  
- `Implementation_codes.ipynb`: Jupyter notebook implementing preprocessing, modeling, and evaluation  
- `requirement.txt`: Python dependencies for setting up the environment  
- `README.md`: Documentation file describing the project  

---

## 5. Preprocessing and Methodology  

### Preprocessing Steps:
- **Textual**:  
  - Lowercasing, stopword removal  
  - Lemmatization, tokenization  
  - Emoji, URL, and HTML tag removal  
  - TF-IDF transformation for feature extraction  

- **Visual**:  
  - Resizing to 224×224 pixels  
  - RGB normalization  
  - Image patch embedding for ViT  

- **Metadata**:  
  - Null value imputation  
  - Min-Max normalization for numeric features  

### Modeling Workflow:
1. Feature extraction from BERT for text and ViT for images  
2. Feature concatenation  
3. PSO-based hyperparameter optimization  
4. Training and evaluation with stratified cross-validation  

---

## 6. Usage Instructions

Follow the steps below to set up and run the project:

---

### 1. Clone the Repository

```bash
git clone https://github.com/AlaaAsimQaffas/FakeProfileDetection-Transformers.git
cd FakeProfileDetection-Transformers

### 2. Install Dependencies

Ensure you have Python ≥ 3.8 installed. Then, install the required libraries:

```bash
pip install -r requirement.txt

### 3. Prepare the Dataset
Place the users.csv files in the following directories:

```bash
Fake_Accounts/users.csv  
Genuine_Accounts/users.csv

### 4. Run the Implementation cells one by one in jupyter notebook file (.ipynb)

```bash
Implementation_codes.ipynb





