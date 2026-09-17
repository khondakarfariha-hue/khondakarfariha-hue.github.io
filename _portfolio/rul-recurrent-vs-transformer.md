---
title: "Recurrent vs Transformer Architectures for Remaining Useful Life Prediction"
excerpt: "A systematic comparison of five deep learning architectures for RUL prediction under Industry 4.0 operating conditions<br/><img src='/images/500x300.png'>"
collection: portfolio
---

A comparative study answering a practically important question in predictive maintenance: does the best deep learning architecture for Remaining Useful Life (RUL) prediction depend on how complex the operating conditions are? Co-authored with Shafiq Mahmud and Rafiatun Ferdous Khan Lubaba, submitted to ICMIME2026.

**Approach:**
- Systematically benchmarked five architectures — LSTM, BiLSTM, GRU, TCN, and Transformer — across all four NASA C-MAPSS turbofan engine degradation subsets, spanning single-condition to six-condition operating environments
- Used engine-wise data partitioning to eliminate temporal leakage, a methodological gap common in prior RUL studies
- Evaluated using RMSE, MAE, R², and the NASA asymmetric scoring function, which penalizes late failure predictions more heavily to reflect real maintenance costs

**Key findings:**
- In homogeneous, single-condition environments, recurrent models remain highly competitive: BiLSTM achieves the lowest RMSE (12.96 cycles), LSTM the lowest NASA score, and GRU the best accuracy-efficiency tradeoff with only ~41K parameters
- As operating complexity increases, the Transformer pulls ahead — achieving 19–32% lower RMSE than recurrent baselines on the most complex subset, and a 57% lower average NASA score under combined heterogeneous training
- Diagnosed and fixed a Transformer "prediction collapse" failure mode on multi-condition data by switching from ReduceLROnPlateau to CosineAnnealingLR scheduling
- Identified the five most influential sensors for RUL prediction via gradient-based feature attribution

The results give practitioners a concrete architecture-selection guideline: recurrent models for resource-constrained, homogeneous systems; Transformers for complex, multi-condition industrial environments.
