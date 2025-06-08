# Commodity-Factors
Enhancing_Commodity_Factor_Strategies_with_Deep_Learning__Evidence_from_Basis_Momentum

# 📈 Enhancing Commodity Factor Strategies with Deep Learning: Evidence from Basis-Momentum

This repository contains the full implementation and experimental results for the paper:

**"Enhancing Commodity Factor Strategies with Deep Learning: Evidence from Basis-Momentum"**,  
submitted to *The Journal of Portfolio Management (JPM)*.

The project explores whether deep learning models—specifically LSTM and Transformer architectures—can improve portfolio construction by learning from factor-based commodity futures signals, particularly the **basis-momentum factor**.

---

## 📁 Repository Structure
```
📂 project-root/
├── LSTM_model.ipynb # LSTM model for predicting portfolio positions (H4 / L4)
├── Transformer_model.ipynb # Transformer model with SHAP value analysis
├── shap_tensor_momentum.npy # Saved SHAP tensor (T x 19 x 19)
├── final_train.csv # Input dataset: factor signals and return sequences
├── transformer_model.pth # Trained Transformer model
├── lstm_model.pth # Trained LSTM model
├── result_test_h4.csv # Predicted H4 strategy returns
├── result_test_l4.csv # Predicted L4 strategy returns
├── result_test_h4_l4.csv # Predicted H4-L4 long-short strategy returns
└── reference_paper.pdf # Final research paper (JPM submission)
```

---

## 🧠 Project Summary

- **Objective**: Enhance traditional rule-based factor investing by using deep learning to rank and select assets based on the basis-momentum factor.
- **Models Used**: 
  - LSTM (baseline sequential model)
  - Transformer (attention-based sequence model with SHAP interpretability)
- **Factor Input**: Monthly basis and momentum values over 12 months
- **Output**: Asset ranking signals (long/short positions) for portfolio construction
- **Evaluation Metric**: Average monthly/annual return and Sharpe ratio of H4 / L4 / H4-L4 portfolios

---

## 📊 SHAP Analysis

Using the trained Transformer model, SHAP values were computed to explain the contribution of input factors (12×19 sequence) to each predicted asset signal.  
Boxplots and heatmaps for full and sub-periods (2022–2025) are included in the `/shap_output/` folder. -> this will be added soon.

---

## 📌 Citation

If you use this project, please consider citing the paper:
SooBeen Kim, “Enhancing Commodity Factor Strategies with Deep Learning: Evidence from Basis-Momentum”, 2025, under review at Journal of Portfolio Management.

---

## 🔧 Requirements

- Python 3.8+
- PyTorch
- SHAP
- scikit-learn
- NumPy, Pandas, Matplotlib, Seaborn

---

## 📬 Contact

For any inquiries, contact **SooBeen Kim** at `rlatnqls010413@gmail.com`.
