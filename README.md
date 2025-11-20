# **Persian Instrument Classification**
**Bachelor Thesis — Mehdi Tootkar Bidarigh**

---

## **Introduction**
This project was developed as part of my Bachelor of Science thesis. The goal is to classify traditional Persian musical instruments using audio recordings.  
The system applies feature extraction techniques such as MFCC and Mel-Spectrograms, and evaluates deep learning models (CNN and CRNN) to identify instruments including Ney, Tar, Setar, Kamancheh, Santur, and Ud.

---

## **Method Overview**

### **1. Audio Preprocessing**
- Loading audio samples  
- Extracting MFCCs (40 coefficients)  
- Optional augmentations (pitch shift, time stretch, noise)

### **2. Model Training**
Two models were tested:
- **CNN** for MFCC-based classification  
- **CRNN** combining convolutional layers with GRU units  

Both models were trained and evaluated using the PCMIR dataset.

### **3. Evaluation**
Performance was measured using:
- Accuracy  
- Precision / Recall / F1  
- Confusion matrix  
- Per-class metrics  

`images/confusion_matrix.png`
`images/per_class_scores.png`

---

## **Dataset**
This project uses the **Persian Classical Music Instrument Recognition (PCMIR)** database.

**Cite as:**

Seyed Muhammad Hossein Mousavi, V. B. Surya Prasath and Seyed Muhammad Hassan Mousavi,  
_"Persian Classical Music Instrument Recognition (PCMIR) Using a Novel Persian Music Database"_,  
ICCKE 2019, Mashhad.

---

## **Dashboard**
A Plotly-based dashboard is included for interactive analysis:
- Interactive confusion matrix  
- Per-class metrics (precision, recall, F1)  
- Visual exploration of model outputs  

`images/dashboard_screenshot.png`

---

## **Usage**
Install the required libraries:
```
pip install -r requirements.txt
```

Place the PCMIR dataset inside a folder named `pcm_dataset`, then run the notebook:
```
notebooks/instruments_sound_classification.ipynb
```

Or train via script:
```
python src/train.py --dataset_dir data/pcm_dataset --model cnn
```

---

## **References**
- Su, Y. (2023). _Instrument Classification Using Different Machine Learning and Deep Learning Methods._  
- Mousavi et al. (2019). _PCMIR: Persian Classical Music Instrument Recognition._

---

## **Acknowledgment**
This work was completed as part of the Bachelor of Science thesis of **Mehdi Tootkar Bidarigh**.
