# 📘 Cognitive Load Detection via Eye Movements

A deep learning pipeline to detect cognitive load from binocular eye-tracking data using temporal models and explainable AI. Designed for real-world applications such as education, healthcare, and cognitive screening.

---

## 👤 About Me

**Aryan Lodha**  
Incoming Graduate, MSc Data Science — University of Bristol  
📧 aryanlodha881@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/aryan-lodha-31b6361b8/) • [GitHub](https://github.com/aryanlodha881](https://github.com/ary0912)

**Role in this project:**
- Designed end-to-end pipeline
- Built feature engineering modules
- Implemented and tuned classical + deep models
- Led explainability and visual storytelling

---

## 🧪 Model Performance

| Model              | Accuracy | F1 Score | ROC-AUC |
|-------------------|----------|----------|---------|
| Logistic Regression | 84.6%   | 0.83     | 0.85    |
| Random Forest       | 93.2%   | 0.93     | 0.94    |
| CNN + LSTM          | 95.5%   | 0.96     | 0.96    |
| TCN                 | 96.9%   | 0.97     | 0.97    |
| **Hybrid TCN+ViT**  | **98.8%** | **0.99** | **0.99** |

✅ Subject-wise train/test split used (no identity leakage)  
✅ 5-fold cross-validated

---

## 🔍 Explainability

### SHAP (for classical models):
- Blink rate and gaze velocity dominate
- Fixation entropy useful in high-load states

### GradCAM++ (for deep models):
- Temporal saliency maps show peaks aligned with cognitive effort
- Attention on blink bursts, pupil constriction, and scan paths

---

## 📊 Visual Insights

- 📉 **Entropy**: right-skewed under high load
- 🔁 **Blink suppression** indicates sustained attention
- 🔭 **Jerkiness** flags decision conflicts
- 🔗 **Scatter plots** reveal clustering in feature space

---

## 🤯 Challenges & Solutions

| Challenge                        | Mitigation                                      |
|----------------------------------|--------------------------------------------------|
| Noisy or missing gaze frames     | Linear interpolation + blink-based masking       |
| Subject overfitting              | Subject-wise data splits                         |
| Redundant features               | PCA and SHAP for dimensionality reduction        |
| Deep learning black-box issues   | SHAP + GradCAM++ for transparency                |

---

## 🌱 Future Work

- 📱 Real-time deployment via mobile/tablet
- 🧬 Cognitive disorder screening (Alzheimer’s, MCI)
- 🎥 Eye + EEG + facial EMG fusion
- 🌐 Cloud-hosted demos (Flask/Streamlit)

---

## 🧠 Dataset

**EM-COGLOAD (Miles et al., 2024)**  
Raw binocular eye-tracking across videos under low and high cognitive load  
- Trials: `data/trials/`
- Repeats: `data/repeats/`  
- Format: `<participant_id>_<task_id>.csv`  
  - `_0` = Low Load (Video A), `_2` = High Load (Video A)  
  - `_1` = Low Load (Video B), `_3` = High Load (Video B)

---

## ⚙️ Repository Structure

cognitive-load-eye-tracking/
├── data/
│   ├── trials/              # Raw trial data (CSV files like 021_0.csv, 045_3.csv)
│   └── repeats/             # Repeated trials for intra-subject validation
│
├── explore3.ipynb           # Feature engineering (velocity, blink rate, entropy, etc.)
├── explore4.ipynb           # Classical ML (Logistic Regression, Random Forest, SHAP)
├── explore5.ipynb           # Deep learning (TCN, ViT), GradCAM++ explanations
│
├── requirements.txt         # Python dependencies
├── README.md                # Project documentation (you're here!)
└── LICENSE                  # MIT license for open-source reuse


---

## 📎 Acknowledgements

- Dr. Gabriella Miles — Research Supervisor  
- Miles et al. (2024) — For the EM-COGLOAD dataset  
- TensorFlow, SHAP, GradCAM++ — Open-source frameworks  
- University of Bristol — Research support
---

_This project demonstrates deep domain knowledge in cognitive science, signal processing, and machine learning. If you’re hiring for AI, healthcare tech, or applied ML roles — let’s talk._
