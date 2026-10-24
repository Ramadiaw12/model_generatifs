# model_generatifs
# 🧠 PyTorch — Discriminative & Generative Models

<p align="center">
  <strong>From Classification to Latent Space Generation</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.12-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/PyTorch-Deep%20Learning-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" alt="PyTorch"/>
  <img src="https://img.shields.io/badge/UV-Dependency%20Management-DE5FE9?style=for-the-badge&logo=astral&logoColor=white" alt="UV"/>
  <img src="https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white" alt="Jupyter"/>
</p>

---

## 🎯 About the Project

This project explores the fundamentals of **deep learning with PyTorch**, progressing from supervised classification to generative modeling.

Through a structured Jupyter Notebook, the goal is to understand how neural networks learn representations, reconstruct input data, and generate new samples from a learned latent space.

The project is organized into three complementary experiments:

- 🔎 **Discriminative Model** — Learn to classify input data and evaluate predictive performance.
- 🔄 **Simple Autoencoder** — Learn compressed representations and reconstruct input samples.
- 🎨 **Variational Autoencoder (VAE)** — Learn a probabilistic latent space to enable structured sampling and data generation.

The project uses **UV** for Python dependency management and reproducible development.

## 🗺️ Learning Roadmap

| Part | Experiment | Main Objective |
|---|---|---|
| 01 | Dataset Loading | Load, inspect and prepare the dataset |
| 02 | Discriminative Model | Train and evaluate a classifier |
| 03 | Simple Autoencoder | Encode, reconstruct and explore representations |
| 04 | Variational Autoencoder | Learn a probabilistic latent space and generate samples |

## 🧪 Experiments

### 01 — Dataset Preparation

Prepare the data before training the models.

- Load the dataset using the appropriate PyTorch utilities.
- Inspect the structure, dimensions and distribution of the data.
- Apply the necessary preprocessing and transformations.
- Create data loaders for efficient training and evaluation.

### 02 — Discriminative Model

Build a neural network that learns to predict class labels from input data.

**Objectives:**
- Define the model architecture.
- Choose an appropriate loss function and optimizer.
- Train the model using backpropagation.
- Evaluate classification performance on test data.
- Measure accuracy using `torcheval.metrics.MulticlassAccuracy`.

**Key concepts:** supervised learning, logits, loss functions, gradient descent, backpropagation and classification metrics.

### 03 — Simple Autoencoder

Build an autoencoder that learns to compress data into a lower-dimensional representation and reconstruct the original input.

**Architecture:**

`Input → Encoder → Latent Representation → Decoder → Reconstruction`

**Objectives:**
- Implement the encoder and decoder.
- Train the model to minimize reconstruction error.
- Evaluate reconstruction quality.
- Explore latent representations.
- Compare original samples with their reconstructions.

**Key concepts:** representation learning, dimensionality reduction, latent space and reconstruction loss.

### 04 — Variational Autoencoder (VAE)

Extend the autoencoder approach with a probabilistic latent representation.

Unlike a standard autoencoder, a VAE learns the parameters of a latent probability distribution and samples from that distribution to generate data.

**Architecture:**

`Input → Encoder → μ and log σ² → Sampling → Decoder → Reconstruction`

**Objectives:**
- Implement the encoder and decoder.
- Learn the latent distribution parameters.
- Apply the reparameterization trick.
- Optimize the reconstruction loss and KL divergence.
- Evaluate reconstruction quality.
- Explore the latent space and generate new samples.

The VAE objective combines two terms:

- **Reconstruction loss:** encourages the generated reconstruction to resemble the input.
- **KL divergence:** regularizes the learned latent distribution toward a prior distribution.

**Key concepts:** probabilistic modeling, latent distributions, reparameterization, KL divergence and generative modeling.

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| PyTorch | Neural networks, automatic differentiation and training |
| Torchvision | Dataset utilities and image transformations |
| Torcheval | Model evaluation metrics |
| NumPy | Numerical operations |
| Matplotlib | Loss curves and visualizations |
| Jupyter Notebook | Interactive experimentation |
| UV | Dependency and project management |

## 📁 Project Structure

```text
.
├── pyproject.toml       # Project metadata and dependencies
├── uv.lock              # Reproducible dependency versions
├── README.md            # Project documentation
└── notebooks/
    └── generative_models.ipynb
                         # Classification, Autoencoder and VAE
```

*The structure above is a suggested organization. Adapt the notebook name and paths to match your actual project.*

## ⚙️ Installation & Setup

### Prerequisites

- Python 3.12
- [UV](https://docs.astral.sh/uv/)
- Git
- Jupyter Notebook support

### 1. Clone the repository

```bash
git clone https://github.com/Ramadiaw12/model_generatifs.git
cd model_generatifs
```

### 2. Initialize the project with UV

If the project has not been initialized yet:

```bash
uv init --name model-generatifs
```

If `pyproject.toml` already exists, skip this step.

### 3. Install dependencies

```bash
uv add torch torchvision torcheval numpy matplotlib jupyter ipykernel
```

### 4. Register the Jupyter kernel

```bash
uv run python -m ipykernel install --user \
  --name model-generatifs \
  --display-name "Python (model-generatifs)"
```

### 5. Launch Jupyter

```bash
uv run jupyter notebook
```

Open the notebook in the `notebooks/` directory and select the **Python (model-generatifs)** kernel.

> **Note:** PyTorch installation may require a platform-specific choice depending on your operating system and whether you intend to use a CPU or a compatible NVIDIA GPU. Consult the [official PyTorch installation guide](https://pytorch.org/get-started/locally/).

## 📊 What You Will Learn

By completing this project, you will develop practical skills in:

- Building and training neural networks with PyTorch.
- Understanding loss functions, optimizers and backpropagation.
- Evaluating classifiers using quantitative metrics.
- Learning compact representations through autoencoders.
- Understanding probabilistic latent spaces in VAEs.
- Visualizing training behavior and reconstruction results.
- Comparing discriminative and generative approaches to deep learning.
- Managing a reproducible Python environment with UV.

## 🔬 Key Takeaway

**Discriminative models learn to predict. Autoencoders learn to reconstruct. Variational autoencoders learn structured latent distributions from which new samples can be generated.**

Together, these experiments provide a practical introduction to the foundations of deep learning and generative modeling.

## 👩‍💻 Author

**Ramatoulaye**

Final-year engineering student in Computer Science & Artificial Intelligence, interested in AI infrastructure, machine learning and generative AI.

- GitHub: [@Ramadiaw12](https://github.com/Ramadiaw12)

---

<p align="center">
  <i>Learning by building. Understanding by experimenting. Growing through deep learning.</i>
</p>