# Long Short-Term Memory Networks (LSTMs): Solving the Vanishing Gradient Problem

## 🎯 Project Overview

This repository contains the materials for the Machine Learning Assignment focusing on **Sequential Data Modeling**.

The primary goal of this project is to provide a detailed tutorial and empirical demonstration of **Long Short-Term Memory (LSTM) Networks**, specifically addressing their core utility: **how the internal gating mechanism effectively solves the Vanishing Gradient Problem** encountered in simple Recurrent Neural Networks (RNNs).

The demonstration uses a sequence classification task (IMDB Sentiment Analysis) to prove the LSTM's superior ability to learn and retain **Long-Term Dependencies**.

---

## 📚 Repository Contents

The repository is structured to provide both a theoretical report and practical, reproducible code.

| File/Folder | Description |
| :--- | :--- |
| `lstm_tutorial_report.pdf` | **The final assignment report ($\approx 1900$ words).** Contains the full theoretical explanation, mathematical background, and analysis of the LSTM architecture. |
| `lstm_comparison_code.ipynb` | **Executable Python code (Jupyter Notebook).** This file implements and trains both the LSTM and a SimpleRNN baseline model on the IMDB dataset for a direct performance comparison. |
| `lstm_rnn_performance_comparison.png` | **Key Empirical Result.** The generated plot showing the Validation Loss and Accuracy curves for the LSTM vs. SimpleRNN across training epochs. |
| `REFERENCES.md` | A complete list of all scholarly articles and online sources used, formatted using the Harvard citation style. |

---

## ⚙️ Running the Code

The code is contained within the `lstm_comparison_code.ipynb` Jupyter Notebook.

### Prerequisites

You will need Python 3 and the following core libraries installed:
* `tensorflow` (or `keras`)
* `numpy`
* `matplotlib`
* `jupyter` (to run the notebook)

You can install the dependencies using `pip`:

```bash
pip install tensorflow numpy matplotlib jupyter

git clone [https://github.com/chavaanilkumar/Long-Short-Term-Memory-Networks-Conquered-the-Vanishing-Gradient]
cd Long Short-Term Memory Networks Conquered the Vanishing Gradient

Open and Run: Open the lstm_comparison_code.ipynb file and execute all cells sequentially. The script will:

Load and preprocess the IMDB dataset.

Define and train the LSTM Model.

Define and train the SimpleRNN Model (baseline).

Generate and display the comparative performance plot (lstm_rnn_performance_comparison.png).

Key Findings and Results
The empirical results from the code demonstrate the necessity of the LSTM's gating mechanism for long sequence modeling:

Model,Problem Solved,Final Test Accuracy (Approximate)
SimpleRNN,Vanishing Gradient,≈70.2%
LSTM Network,Long-Term Dependencies,≈87.5%


As shown in the generated plot, the SimpleRNN quickly stagnates due to the vanishing gradient, failing to propagate error signals back to early time steps in the long movie reviews. The LSTM, by using its Cell State and Gates, maintains a healthy gradient flow, resulting in an over 17% absolute increase in classification accuracy on the test set.

License: This project is licensed under the MIT License - see the LICENSE file for details.
