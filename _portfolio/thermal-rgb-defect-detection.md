---
title: "Thermal + RGB Fusion for Industrial Defect Detection"
excerpt: "Dual-stream deep learning for multi-modal defect detection<br/><img src='/images/500x300.png'>"
collection: portfolio
---

Research project developing a multi-modal deep learning approach to industrial defect detection, combining thermal and RGB (visible-light) imaging to catch defects that either sensor alone would miss.

**Approach:**
- Dual-stream ResNet-50 architecture, one stream for thermal input and one for RGB input
- A Cross-Modal Attention Module fuses information from both streams at the feature level, allowing each modality to inform the other during detection
- Feature-level fusion strategy, chosen over simpler early or late fusion for stronger cross-modal interaction

Currently being written up for submission to an IEEE/ACM conference.
