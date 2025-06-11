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


## 6. 📚 Citations

If you use this dataset or model in your research, please cite the following:

```bibtex
@article{yourstudy2025fakeprofile,
  title={Social media Fake Profile Detection using Transformer-based Model and Parameters Optimization},
  author={Alaa Asim Qaffas},
  journal={PeerJ Computer Science},
  year={2025},
  publisher={PeerJ, Inc.}
}
```

Additionally, refer to the Cresci-2017 dataset if used:

```bibtex
@inproceedings{cresci2017paradigm,
  title={The paradigm-shift of social spambots: Evidence, theories, and tools for the arms race},
  author={Cresci, Stefano and Di Pietro, Roberto and Petrocchi, Marinella and Spognardi, Angelo and Tesconi, Maurizio},
  booktitle={Proceedings of the 26th international conference on World Wide Web companion},
  pages={963--972},
  year={2017}
}
```

---

## 7. 🔧 Usage Instructions

Follow the steps below to set up and run the Fake Profile Detection using Transformers project.

### 📁 1. Clone the Repository

First, clone the repository and navigate into the project directory:

```bash
git clone https://github.com/AlaaAsimQaffas/FakeProfileDetection-Transformers.git
cd FakeProfileDetection-Transformers
```

---

### 📦 2. Install Dependencies

Ensure that **Python 3.8 or later** is installed on your system. It is recommended to use a virtual environment for managing dependencies.

Install the required Python libraries using `pip`:

```bash
pip install -r requirement.txt
```

> 💡 Tip: If you're using a virtual environment, activate it before running the above command.

---

### 📂 3. Prepare the Dataset

You need to manually place the `users.csv` files into the appropriate directories before running the implementation.

Ensure the following directory structure:

```
FakeProfileDetection-Transformers/
├── Fake_Accounts/
│   └── users.csv
├── Genuine_Accounts/
│   └── users.csv
```

Place your respective fake and genuine user datasets in the `users.csv` files as shown above.

---

### 🚀 4. Run the Jupyter Notebook

Launch Jupyter Notebook and open the implementation file:

```bash
jupyter notebook
```

Then, open and execute the following notebook cell by cell:

```
Implementation_codes.ipynb
```

> 📌 Make sure the dataset is properly loaded and all dependencies are resolved before running each cell.

---

### ✅ Done!

You should now be able to run the full implementation for detecting fake profiles using transformer models. For any issues or enhancements, feel free to raise an issue or contribute to the repository.






