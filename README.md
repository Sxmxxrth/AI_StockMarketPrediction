<div align="center">

# 📈 AI Stock Market Prediction

[![Python Version](https://img.shields.io/badge/Python-3.9+-blue.svg?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Docker Support](https://img.shields.io/badge/Docker-Supported-2496ED.svg?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Lab-F37626.svg?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-FF6F00.svg?style=for-the-badge&logo=tensorflow&logoColor=white)](https://www.tensorflow.org/)

*Predicting stock closing prices using Deep Learning (FCNN, LSTM, CNN) and Time-Series Analysis.*

</div>

---

## 📖 Overview

This project implements various advanced Machine Learning and Deep Learning architectures to analyze historical stock market data and predict future prices. The core objective is to predict the **[Close]** price of a given day based on the previous 7 days of features: `[Open, High, Low, Volume, Close]`.

### Key Highlights
- **Comprehensive EDA:** Unsupervised analysis of Nifty 50 stocks.
- **Deep Learning Architectures:** Includes implementations for Fully Connected Neural Networks (FCNN), Convolutional Neural Networks (CNN), Long Short-Term Memory networks (LSTM), and hybrid CNN-LSTM models.
- **Robust Evaluation:** Results are benchmarked using Root Mean Squared Error (RMSE) and Regression Lift Charts on the test set.

---

## 🏗️ Architecture & Approach

Our models are trained on structured time-series data to capture temporal dependencies in stock movements.

1. **Data Preprocessing:** Data is cleaned, normalized, and engineered into rolling windows (7-day sequences).
2. **Model Training:** 
    - **FCNN:** Baseline deep learning model for feature mapping.
    - **CNN:** Extracts spatial/structural patterns in short-term price movements.
    - **LSTM / RNN:** Captures long-term sequential dependencies in time-series data.
    - **Hybrid:** Combines CNN's feature extraction with LSTM's sequential modeling.
3. **Evaluation:** Detailed visual charts (Lift Charts, Regression Plots) are generated to compare expected vs. predicted outputs.

---

## 🚀 Quick Start (Docker)

We provide a fully containerized environment using **Docker** and **Docker Compose**. This ensures you don't have to worry about complex dependency management or environment conflicts.

### Prerequisites
- [Docker](https://docs.docker.com/get-docker/) installed on your machine.
- [Docker Compose](https://docs.docker.com/compose/install/) installed.

### Setup Instructions

1. **Clone the Repository:**
   ```bash
   git clone <your-repo-url>
   cd AI_StockMarketPrediction
   ```

2. **Start the Environment:**
   Run the following command to build the Docker image and start the Jupyter Lab server.
   ```bash
   docker-compose up --build
   ```

3. **Access Jupyter Lab:**
   Open your browser and navigate to:
   ```text
   http://localhost:8888
   ```
   *Note: Authentication is disabled by default for ease of local development.*

4. **Stop the Environment:**
   ```bash
   docker-compose down
   ```

---

## 📁 Repository Structure

```text
AI_StockMarketPrediction/
│
├── Dockerfile                             # Docker configuration
├── docker-compose.yml                     # Multi-container orchestration
├── requirements.txt                       # Python dependencies
├── nifty_50_unsupervised_analysis_.ipynb  # Unsupervised learning on Nifty 50
├── README.md                              # Project documentation
└── P2_CodeBase/                           # Source code and experiments
    ├── data/                              # Dataset directory
    ├── P2_NeuralNetworks.ipynb            # FCNN Models
    ├── P2_CNN.ipynb                       # CNN Models
    ├── P2_HyperParameter_LSTM.ipynb       # LSTM tuning & training
    ├── P2_RNN-LSTM.ipynb                  # RNN & LSTM comparisons
    └── ... (other preprocessing and helper scripts)
```

---

## 📊 Results

The notebooks within `P2_CodeBase` generate comprehensive evaluation charts. You will find:
- **RMSE Scores:** To quantify the model's prediction error.
- **Regression Lift Charts:** Plotting expected outputs vs. predictions to visually assess model tracking performance.
- **Confusion Matrices & Classification Reports:** For specific sub-tasks involving binary/multiclass categorical predictions.

---

<div align="center">
  <i>Developed with ❤️ for Time-Series Analysis & MLOps</i>
</div>
