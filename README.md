# An Attention-Based Deep Learning Model for Multi-Horizon Prediction of Load, Price, and Wind Power Generation in Smart Grids

This repository contains the official implementation of the paper:

**An Attention-Based Deep Learning Model for Multi-Horizon Prediction of Load, Price, and Wind Power Generation in Smart Grids**

📌 *Selected as a Best Paper*  
📍 29th International Electrical Power Distribution Conference (EPDC 2025), Tehran, Iran

---

## 🔗 Paper Information

- **DOI:** 10.1109/EPDC67173.2025.11278281  
- **IEEE Xplore:** https://ieeexplore.ieee.org/abstract/document/11278281  
- **Conference:** EPDC 2025  
- **Authors:**  
  - Mozhgan Rahmatinia  
  - Seyed-Amin Hosseini-Seno  

---

## 🧠 Abstract

Accurate forecasting of electricity load, price, and renewable energy generation is a key requirement for demand response and stability in smart grids.  
This work proposes a novel **attention-based encoder–decoder deep learning model** enhanced with **Fast Fourier Transform (FFT)** preprocessing to simultaneously predict:

- Electricity Load  
- Electricity Price  
- Wind Power Generation  

The model captures both **short-term fluctuations** and **long-term temporal dependencies**, outperforming several state-of-the-art models such as LSTM, CNN-LSTM, LSTM-Attention, and vanilla Seq2Seq across multiple European datasets.

---

## ✨ Key Contributions

- 🔹 Simultaneous multi-output forecasting (load, price, wind)
- 🔹 Multi-horizon prediction (12, 24, 48 hours ahead)
- 🔹 FFT-based frequency-domain preprocessing for noise reduction
- 🔹 Encoder–Decoder architecture with stacked **BiLSTM**
- 🔹 Scaled Attention mechanism for long-term dependency modeling
- 🔹 Extensive evaluation on real-world datasets from four countries

---

## 🏗️ Model Architecture

The proposed model consists of four main components:

<img width="525" height="651" alt="image" src="https://github.com/user-attachments/assets/fe604656-88e7-4ef0-a395-3e387dfd3cac" />


1. **FFT Preprocessing**  
   Transforms historical input data into the frequency domain to extract dominant periodic and seasonal patterns.

2. **Encoder (BiLSTM Stack)**  
   Captures forward and backward temporal dependencies and encodes multivariate input sequences.

3. **Scaled Attention Mechanism**  
   Dynamically assigns importance weights to encoder outputs, highlighting the most influential temporal features.

4. **Decoder (BiLSTM)**  
   Generates future predictions for load, price, and wind generation directly in the time domain.

---

## 📊 Datasets

Experiments were conducted using real-world data from **Open Power System Data (OPSD)**:

- 🇦🇹 Austria (AT)
- 🇮🇹 Italy – Central North (IT-CNOR)
- 🇸🇪 Sweden (SE_2)
- 🇬🇧 United Kingdom (GB)

**Specifications:**
- Time resolution: 60 minutes  
- Duration: ~5 years (2015–2020)  
- Train/Test split: 80% / 20%  
- Validation: 20% of training data  

---

## 📈 Evaluation Metrics

Model performance is evaluated using:

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- Pearson Correlation Coefficient (r)

---

## 🧪 Experimental Results

The proposed model consistently outperforms baseline methods, especially for **short- to mid-term horizons (12–48 hours)**.

✔ Superior accuracy on AT, IT, and GB datasets  
✔ Competitive performance on SE_2  
✔ Strong capability in tracking real-world temporal trends

---

## 🖥️ Environment

- Python 3.10  
- PyTorch  
- Scikit-learn  
- Google Colab (T4 GPU)

---

## 📂 Repository Structure

```bash
├── data/
│   ├── raw/
│   └── processed/
├── models/
│   ├── encoder.py
│   ├── decoder.py
│   └── attention.py
├── train.py
├── test.py
├── utils.py
├── requirements.txt
└── README.md
```
## 📌 Citation

If you use this work, please cite:
@inproceedings{rahmatinia2025attention,
  title={An Attention-Based Deep Learning Model for Multi-Horizon Prediction of Load, Price, and Wind Power Generation in Smart Grids},
  author={Rahmatinia, Mozhgan and Hosseini-Seno, Seyed-Amin},
  booktitle={2025 29th International Electrical Power Distribution Conference (EPDC)},
  year={2025},
  doi={10.1109/EPDC67173.2025.11278281}
}


## 📬 Contact

Mozhgan Rahmatinia

📧 Email: mozhgan.rahmatinia@mail.um.ac.ir

🔗 GitHub: https://github.com/mozhgan-Rahmatinia
