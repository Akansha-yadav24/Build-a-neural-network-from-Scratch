# 🧠 Neural Network From Scratch — Pure Python

> No NumPy. No TensorFlow. No shortcuts. Just Python and Maths.

Build a fully working neural network from absolute zero — weights, forward pass, backpropagation, gradient descent, all of it. By the end, the network learns to solve the XOR problem on its own.

---

## 📁 File

| File | Description |
|------|-------------|
| `neurons.ipynb` | Complete code — step by step, chapter by chapter |

---

## 🎯 What This Covers

- What a neuron is and how it works mathematically
- Sigmoid activation function
- Building a Layer and a full NeuralNetwork class
- Forward pass — how data flows through the network
- Loss function — Mean Squared Error (MSE)
- Backpropagation — chain rule explained and coded
- Gradient descent — how weights get updated
- Full training loop — watch the loss drop in real time
- Solving the XOR problem — a classic non-linear task

---

## 🧮 Key Formulas

```
Neuron output:       z = (w1×x1) + (w2×x2) + ... + bias
Sigmoid:             σ(z) = 1 / (1 + e^−z)
Sigmoid derivative:  σ'(z) = σ(z) × (1 − σ(z))
MSE Loss:            L = (1/n) × Σ(y − ŷ)²
Weight update:       w = w + α × δ × x
```

---

## 🏗️ Network Architecture

```
Input Layer    Hidden Layer    Output Layer
  (2 neurons) → (4 neurons)  → (1 neuron)

  x1 ─┐
       ├──→ [h1]─┐
  x2 ─┤    [h2] ├──→ [ŷ]
       ├──→ [h3]─┘
       └──→ [h4]
```

---

## ▶️ How to Run

**Option 1 — Jupyter Notebook (recommended)**
```bash
jupyter notebook neural_network_from_scratch.ipynb
```

**Option 2 — VS Code**
Open the `.ipynb` file directly in VS Code with the Jupyter extension.

**Option 3 — Google Colab**
Upload the file to [colab.research.google.com](https://colab.research.google.com) and run all cells.

No installations needed — only Python standard library (`math`, `random`).

---

## 📊 Expected Output

After 10,000 epochs of training:

```
Epoch      0  |  Loss: 1.248631
Epoch   2000  |  Loss: 0.009072
Epoch   4000  |  Loss: 0.003215
Epoch   6000  |  Loss: 0.001905
Epoch   8000  |  Loss: 0.001342
Epoch  10000  |  Loss: 0.001031

[0, 0] => 0.0092   Expected: 0  ✅
[0, 1] => 0.9857   Expected: 1  ✅
[1, 0] => 0.9841   Expected: 1  ✅
[1, 1] => 0.0221   Expected: 0  ✅
```

---

## 📓 Notebook Structure

| Cell | Topic |
|------|-------|
| 1 | Imports |
| 2 | Neuron class |
| 3 | Layer class |
| 4 | NeuralNetwork class (forward + backward + update) |
| 5 | XOR dataset |
| 6 | Loss function (MSE) |
| 7 | Backprop verification |
| 8 | Training loop |
| 9 | ASCII loss curve |
| 10 | Final test — all 4 XOR predictions |
| 11 | Bonus experiments (learning rates, hidden sizes) |

---

## 🧪 Bonus Experiments (inside the notebook)

**Try different learning rates:**
```
lr=0.1  → trains slowly
lr=0.5  → sweet spot
lr=2.0  → might overshoot
```

**Try different hidden layer sizes:**
```
[2, 2, 1]  → barely enough neurons
[2, 8, 1]  → more capacity
[2, 16, 1] → overkill for XOR, but works
```

---

## 📋 Prerequisites

- Basic Python (for loops, classes, functions)
- High school algebra
- That's it — no calculus background needed

---

## 🗺️ What's Next

Once you understand this, you're ready for:

- Vectorizing with NumPy (same logic, 100x faster)
- Multi-class classification with Softmax
- Convolutional Neural Networks (CNNs)
- Building a tiny GPT from scratch

---

## 📜 License

MIT — free to use, share, and modify.

---

*Built as a companion to the "Neural Network From Scratch" YouTube video series.*
