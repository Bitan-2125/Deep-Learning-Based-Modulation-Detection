# Modulation Detection Using Deep Learning

This research-based project explores **Automatic Modulation Classification (AMC)** using state-of-the-art Deep Learning architectures. By leveraging the RadioML datasets, we compare the effectiveness of spatial and temporal feature extraction in identifying modulation techniques in noisy wireless environments.

## 👥 Authors
* [cite_start]**Bitan Das** - The LNM Institute of Information Technology (LNMIIT) [cite: 7, 10]
* [cite_start]**Jaiveer Singh** - The LNM Institute of Information Technology (LNMIIT) [cite: 7, 10]
* [cite_start]**Mentor:** Dr. Vaibhav Kumar Gupta [cite: 9]

---

## 📌 Project Overview
[cite_start]Modern radio receivers require robust AMC to identify modulation techniques without prior signal knowledge[cite: 22, 37]. [cite_start]This project implements and evaluates three distinct deep learning models to classify raw $I/Q$ signal samples across varying Signal-to-Noise Ratios (SNR)[cite: 38, 69].

### Key Features:
* [cite_start]**Adaptive Evaluation:** Per-SNR performance analysis[cite: 40].
* [cite_start]**Feature Visualization:** Channel-wise visualization of Conv1D $I/Q$ kernels and L1-norm filter-strength ranking[cite: 40].
* [cite_start]**Multimodal Architectures:** Implementation of CNN, LSTM, and hybrid CLDNN models[cite: 25].

---

## 📊 Datasets
[cite_start]We utilized the industry-standard **RadioML** datasets provided by O'Shea and West[cite: 243]:
* [cite_start]**RadioML2016.10a:** 11 modulation classes (BPSK, QPSK, 8PSK, 16QAM, 64QAM, BFSK, CPFSK, PAM4, WB-FM, AM-SSB, AM-DSB)[cite: 70, 111].
* [cite_start]**RadioML2016.10b:** A larger version with 10 classes, offering more examples per SNR for robust training[cite: 70, 171].
* [cite_start]**SNR Range:** -20 dB to +18 dB[cite: 69].

---

## 🏗️ Model Architectures

| Model | Description | Parameters |
| :--- | :--- | :--- |
| **CLDNN** | [cite_start]Combines Conv1D (spatial) and LSTM (temporal) layers for maximum robustness[cite: 83, 87]. | [cite_start]97,547 [cite: 86] |
| **MCNN** | [cite_start]A 7-layer specialized CNN designed for low-SNR robustness[cite: 89, 90]. | [cite_start]336,396 [cite: 93] |
| **Pure LSTM** | [cite_start]Relies entirely on recurrent layers to capture long-range dependencies in $I/Q$ data[cite: 96, 97]. | [cite_start]207,627 [cite: 99] |

---

## 📈 Performance & Results
* [cite_start]**CLDNN** emerged as the top performer, particularly at low SNR, due to its ability to mirror human expert analysis—first noticing waveform details and then tracking behavioral consistency over time[cite: 30, 217].
* [cite_start]**MCNN** provided competitive accuracy with higher computational efficiency[cite: 218].
* [cite_start]**Pure LSTM** highlighted the necessity of convolutional pre-processing, as it struggled with raw $I/Q$ data compared to the hybrid approach[cite: 220, 233].

---

## 🚀 Future Work
* [cite_start]**Hardware Deployment:** Implementing models on SDR hardware like USRP or RTL-SDR[cite: 238].
* [cite_start]**Edge Optimization:** Quantizing models for efficient inference on mobile and edge devices[cite: 240].
* [cite_start]**Advanced Modeling:** Exploring Transformer-based architectures to push recognition limits[cite: 236].

---

## 📚 References
1. [cite_start]T. O'Shea, N. West, "RadioML2016.10a and 2016.10b Datasets"[cite: 243].
2. [cite_start]Sainath et al., "Convolutional, Long Short-Term Memory, Fully Connected DNNs"[cite: 244].
