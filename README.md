# A Skin Disease Detection Application Using CNN and 20 Skin Diseases Dataset

Skin diseases are a widespread health concern, requiring timely and precise diagnosis for effective management and treatment. This is the codebase for the skin disease detection application that utilizes Convolutional Neural Networks (CNNs) to identify eight types of skin diseases: Acne and Rosacea, Cellulitis Impetigo and other Bacterial Infections, Eczema, Light Diseases and Disorders of Pigmentation, Psoriasis Lichen Planus and related diseases, Seborrheic Keratoses and other Benign Tumors, Urticaria Hives, and Vascular Tumors. The technical architecture of the CNN, dataset preparation, training process, and performance metrics are detailed.

## CNN Architecture
* **Input Layer**
  - Input Shape: 192x192x3 (RGB image)
  
* **Convolutional Layers**
  - Conv Layer 1: 64 filters, 3x3 kernel, ReLU activation, Batch Normalization
  - Conv Layer 2: 128 filters, 2x2 kernel, ReLU activation, Batch Normalization
  - Conv Layer 3: 256 filters, 2x2 kernel, ReLU activation, Batch Normalization
  - Conv Layer 4: 512 filters, 2x2 kernel, ReLU activation, Batch Normalization

* **Pooling Layers**
  - 4 Pooling Layers after Convolutional Blocks: Max pooling, 2x2 window

* **Fully Connected Layers**
  - Dense Layer 1: 256 neurons, ReLU activation
  - Dense Layer 2: 128 neurons, ReLU activation
  - Dense Layer 3: 64 neurons, ReLU activation
  - Dense Layer 4: 8 neurons (softmax activation)
 
## Training the Model
### Hyperparameters
- **Loss Function**: Categorical Cross-Entropy
- **Optimizer**: Adamax
- **Learning Rate**: 0.001
- **Batch Size**: 32
- **Epochs**: 20

## Evaluation
The model's performance was evaluated using accuracy, precision, recall, and F1-score, achieving around 90% accuracy on the test set.

![validation-accuracy-and-loss](https://github.com/SMRSLYMNL/skin-disease-detection/assets/10634784/66025896-6f0f-4b38-ac01-fd41e870f54f) ![training-accuracy-and-loss](https://github.com/SMRSLYMNL/skin-disease-detection/assets/10634784/9c1f3abb-4a76-4d9a-98ac-04fb0be87b10)


