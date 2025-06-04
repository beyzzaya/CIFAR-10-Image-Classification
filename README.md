# CIFAR-10-Image-Classification

his repository contains **`CIFAR-10-Image-Classification.ipynb`**, a step-by-step Jupyter Notebook that
trains a Convolutional Neural Network (CNN) on the **CIFAR-10** dataset  
(airplane ✈️, automobile 🚗, bird 🐦, cat 🐱, deer 🦌, dog 🐶, frog 🐸, horse 🐴,
ship 🚢, truck 🚚).

### Key points
- **Data loading & visual check** – downloads CIFAR-10 via `keras.datasets`,
  displays sample images.  
- **Pre-processing** – normalises pixels (`/255`) and builds a
  `tf.data` pipeline with optional batching.  
- **Model** – three convolution blocks  
  `Conv2D ➜ ReLU ➜ Conv2D ➜ ReLU ➜ MaxPool`, then  
  `Flatten ➜ Dense(128) ➜ Dense(10, softmax)`.  
- **Training** – Adam optimiser, EarlyStopping (`patience=5`) and
  ModelCheckpoint (saves best model).  
- **Result** – reaches **≈ 70 % validation accuracy** in 20 epochs.
