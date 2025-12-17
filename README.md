
# MRI Reconstruction using Complex-valued Convolutional Neural Network

This repository contains the implementation of a cascaded complex-valued Convolutional Neural Network framework for MRI reconstruction. 

1. ## Clone the repository
2. ## Undersampling Mask
     var_sampling_mask.npy                # Undersampling mask used to undersample k-space
3. ## 🏗 Model Construction

The core model architecture is defined using complex-valued layers and activation functions.  
To construct the model, the following notebooks are used:

- `activation.ipynb`: Contains the complex-valued activation functions required by the network.
- `layer.ipynb`: Provides complex-valued helper functions and custom layer definitions.
- `complex_1.ipynb`, `complex_2.ipynb`, and `model_attention1.ipynb`: Define the architecture of the proposed complex-valued reconstruction model.

---

4. ## 🏋️ Model Training

The training procedure for the proposed MRI reconstruction models is implemented using the following notebooks:

- `flat_unrolled_cascade_train_sc.ipynb`: Used for training the cascaded and unrolled reconstruction model.
- `attention_train1.ipynb`: Used for training attention-based reconstruction models, including the proposed complex-valued model.

During training, the scripts load the undersampling mask and the Calgary-Campinas MRI dataset (for both training and validation), create the data generators, and optimize the model parameters.

5. ## 📂 Repository Structure
```text    
├── activation.ipynb                      # Complex-valued activation function implementations
├── attention_train1.ipynb               # Training notebook for attention-based models
├── complex_1.ipynb                      # Complex-valued model
├── complex_2.ipynb                      # Complex-valued model
├── complex_zrelu.ipynb                  # Implementation of complex zReLU activation
├── flat_unrolled_cascade_train_sc.ipynb # Training of flat unrolled cascade model
├── layer.ipynb                          # Complex-valued helper functions and custom layers
├── model_attention1.ipynb               # Attention-based reconstruction model
├── model_cbam_attention2.ipynb          # CBAM attention-based reconstruction model
├── simple_model.ipynb                   # Baseline reconstruction model
├── var_sampling_mask.npy                # Undersampling mask used to undersample k-space
└── README.md                            # Project documentation
