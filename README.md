# Reinforcement Learning Assignment — Deep Q-Network (Pong)

## Student Information

* **Name:** Rohit Iyer
* **Student ID:** 8993045

---

## 📌 Assignment Summary

This assignment focuses on implementing a **Deep Q-Network (DQN)** to train an agent to play the **Pong environment** from OpenAI Gym (Atari).

Unlike tabular Q-learning, Pong uses high-dimensional image inputs. Therefore, a **Convolutional Neural Network (CNN)** is used to approximate the Q-function.

### Key Features Implemented

* Deep Q-Network (DQN) with CNN
* Experience Replay Buffer
* Target Network for stable learning
* ε-greedy exploration strategy
* Frame preprocessing (crop, grayscale, resize)
* Frame stacking (4 frames)

---

## 📊 Experiments Performed

The following experiments were conducted:

### 1. Baseline Training

* Mini-batch size = 8
* Target network update = every 10 episodes

### 2. Hyperparameter Sweeps

* Mini-batch size: **[8, 16]**
* Target update frequency: **[3, 10] episodes**

### Metrics Tracked

* Score per episode
* Average cumulative reward (last 5 episodes)
* Training steps
* Loss

---

## 🏆 Final Conclusion

Based on experimental results:

* **Best Mini-Batch Size:** 16
* **Best Target Update Frequency:** Every 10 episodes

This combination provided:

* More stable learning
* Smoother reward trends
* Better convergence behavior

---

## 🛠️ Requirements

Install dependencies using:

```bash
pip install -r requirements.txt
```

### Required Libraries

* Python 3.11
* torch
* gymnasium[atari]
* autorom
* numpy
* matplotlib
* tqdm

---

## ▶️ How to Run

### Step 1 — Create Virtual Environment (recommended)

```bash
python -m venv .venv
.\.venv\Scripts\activate
```

### Step 2 — Install Dependencies

```bash
pip install -r requirements.txt
```

### Step 3 — Install Atari ROMs

```bash
AutoROM --accept-license
```

### Step 4 — Run Notebook

Open and run:

```bash
Assignment3_Pong_DQN_OOP_NOTEBOOK.ipynb
```

or run all cells in Jupyter Notebook / VS Code.

---

## 📁 Project Structure

```
Assignment3/
│
├── Assignment3_Pong_DQN_OOP_NOTEBOOK.ipynb
├── assignment3_utils.py
├── requirements.txt
├── README.md
└── outputs/
    ├── plots/
    ├── results/
```

---

## ⚠️ Notes

* Ensure Gymnasium Atari environments are properly installed.
* If you encounter environment errors:

  * Install using: `pip install gymnasium[atari]`
  * Run: `AutoROM --accept-license`
* Training may take significant time depending on hardware.

---

## 🚀 Final Remarks

This assignment demonstrates the application of Deep Reinforcement Learning to a complex environment using image-based observations. It highlights the importance of:

* Proper preprocessing
* Stable training techniques
* Hyperparameter tuning

---
