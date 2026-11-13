# LP-IV Deep Learning Practicals

Jupyter Notebook files for the six LP-IV Deep Learning lab assignments.

## Contents
1. Practical 1 — Study of Keras, PyTorch, TensorFlow and Theano
2. Practical 2 — Feedforward Neural Network on MNIST using Keras/TensorFlow and SGD
3. Practical 3 — CNN image classification on MNIST
4. Practical 4 — Autoencoder for anomaly detection (MNIST demonstration)
5. Practical 5 — CBOW Word2Vec using Gensim
6. Practical 6 — Object detection using pre-trained Faster R-CNN (TorchVision)

## Setup on a college lab computer

Use Python 3.10 or 3.11 if possible. Open Command Prompt in this project folder.

```bash
python -m venv .venv
.venv\Scripts\activate
python -m pip install --upgrade pip
pip install notebook
pip install -r requirements.txt
jupyter notebook
```

For Practical 6, install a compatible PyTorch/TorchVision pair using the official selector:
https://pytorch.org/get-started/locally/

Then open the required `.ipynb` file and run cells from top to bottom using Shift+Enter.

## Dataset and internet notes

- Practicals 2, 3 and 4 use MNIST through `tf.keras.datasets.mnist`. TensorFlow downloads it automatically the first time. Internet is required for the first download unless the dataset is already cached.
- Practical 5 uses the included small text corpus at `dataset/corpus.txt`. It does not need a separate dataset download.
- Practical 6 expects an image at `dataset/sample.jpg`. Add your own JPG image there. The first run also downloads pre-trained Faster R-CNN weights, so internet is required unless weights are cached.
- Do not commit large downloaded datasets or model-weight files to GitHub. Keep them locally or use an approved dataset link.

## Important
- Run notebooks from the repository root folder so relative paths to `dataset/` work.
- Theano is a legacy/discontinued library and may not install on modern Python. Practical 1 is a study/theory practical.
- The provided object-detection notebook runs inference with a pre-trained detector. Training/fine-tuning on a custom dataset requires labelled images with bounding-box annotations.
- These notebooks are educational starter implementations. Follow any specific code/format required by your faculty or lab manual.

## GitHub upload
Create a public or private repository, then upload this folder's contents. Alternatively, use GitHub Desktop or `git`:
```bash
git init
git add .
git commit -m "Add LP-IV deep learning practical notebooks"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/LP-IV-Deep-Learning-Practicals.git
git push -u origin main
```
