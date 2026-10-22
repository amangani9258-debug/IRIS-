# 🌸 Iris Petal Length Prediction

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-v1.0%2B-orange.svg)](https://scikit-learn.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

An end-to-end Machine Learning project that uses **Linear Regression** to predict the `petal_length` of Iris flowers based on other physical features like sepal length, sepal width, and petal width.

---

## 📌 Table of Contents
- [About The Project](#-about-the-project)
- [Dataset Overview](#-dataset-overview)
- [Project Architecture & Workflow](#-project-architecture--workflow)
- [Model Performance](#-model-performance)
- [Installation & Getting Started](#-installation--getting-started)
- [How to Run](#-how-to-run)
- [Tech Stack](#-tech-stack)
- [Author & License](#-author--license)

---

## 🔍 About The Project

While the classic **Iris Dataset** is typically used for classification (categorizing flowers by species), this project focuses on **Regression Analysis**. 

The goal is to analyze continuous feature relationships and accurately estimate the target continuous variable (`petal_length`) given other physical dimensions of the flower.

### Key Highlights:
- **Fast & Lightweight:** Built using standard Python scientific libraries.
- **Data Visualization:** Includes plot visualizations to compare **Actual vs. Predicted** values.
- **High Accuracy:** Evaluated with standard metrics ($R^2$ Score & Mean Squared Error).

---

## 📊 Dataset Overview

The dataset is loaded directly using Seaborn (`sns.load_dataset('iris')`).

| Feature | Type | Description |
| :--- | :--- | :--- |
| `sepal_length` | Continuous | Length of the sepal in cm (Input Feature) |
| `sepal_width` | Continuous | Width of the sepal in cm (Input Feature) |
| `petal_width` | Continuous | Width of the petal in cm (Input Feature) |
| `petal_length` | Continuous | **Target Variable** to predict in cm |

---

## 🔄 Project Architecture & Workflow

1. **Data Acquisition:** Fetching the dataset into a Pandas DataFrame.
2. **Feature & Target Split:** 
   - $X = \{\text{sepal\_length}, \text{sepal\_width}, \text{petal\_width}\}$
   - $y = \{\text{petal\_length}\}$
3. **Train-Test Splitting:** $80\%$ Training Data, $20\%$ Testing Data (`random_state=42`).
4. **Model Training:** Fitting a `LinearRegression()` model on the training set.
5. **Model Evaluation:** Metric assessment on the unseen test set.
6. **Visualization:** Plotting predictions against ground truth using Matplotlib/Seaborn.

---

## 📈 Model Performance

The Linear Regression model achieves strong predictive capabilities on the test dataset:

| Metric | Score | Description |
| :--- | :--- | :--- |
| **$R^2$ Score** | `~0.96` | Explains $\approx 96\%$ of the variance in petal length |
| **MSE (Mean Squared Error)** | `~0.13` | Low mean squared prediction error |

---

## ⚙️ Installation & Getting Started

### Prerequisites
Make sure you have Python 3.8+ installed on your system.

### Installation Steps

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/iris-petal-length-prediction.git
   cd iris-petal-length-prediction
   ```

2. **Set up a Virtual Environment (Recommended):**
   ```bash
   # On macOS/Linux
   python3 -m venv venv
   source venv/bin/activate

   # On Windows
   python -m venv venv
   venv\Scripts\activate
   ```

3. **Install Requirements:**
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn jupyter
   ```

---

## 🚀 How to Run

1. Open Jupyter Notebook or Google Colab:
   ```bash
   jupyter notebook
   ```
2. Navigate to and open the project notebook (`.ipynb`).
3. Run all cells sequentially (`Cell > Run All`) to observe data loading, training, model evaluation metrics, and plots.

---

## 🛠️ Tech Stack

- **Language:** Python
- **Data Manipulation:** `pandas`, `numpy`
- **Machine Learning:** `scikit-learn`
- **Data Visualization:** `matplotlib`, `seaborn`
- **Environment:** Jupyter Notebook / Google Colab

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.