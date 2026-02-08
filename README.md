# Image Reconstruction using Autoencoder on Chest X-ray Images

## Project Description
This project demonstrates image reconstruction using a convolutional autoencoder.
A subset of chest X-ray images is used to train the model to learn compact representations
and reconstruct the original images.

## Dataset
- Dataset: Chest X-ray Images (Kaggle)
- Type: Medical Imaging
- Samples used: ~200 normal chest X-ray images
- Images were manually selected from the dataset

Only normal X-ray images were used to simplify reconstruction and avoid class imbalance.

## Preprocessing Steps
- Images converted to grayscale
- Resized to 64 × 64 pixels
- Pixel values normalized to the range [0, 1]
- Converted to PyTorch tensors

## Model Architecture
- Encoder:
  - Convolution layers with ReLU activation
  - Downsampling using stride
- Decoder:
  - Transposed convolution layers
  - Sigmoid activation for reconstruction

## Training Details
- Framework: PyTorch
- Loss Function: Mean Squared Error (MSE)
- Optimizer: Adam
- Train–Validation Split: 80% / 20%
- Epochs: 10

## Results
- The autoencoder successfully reconstructs chest X-ray images
- Reconstructed images appear smoother due to dimensionality reduction
- Reconstruction error is visualized using heatmaps
- Smoothed heatmaps highlight regions with higher reconstruction error

## Conclusion
This project shows how autoencoders can learn compact representations of medical images
and reconstruct them with reasonable accuracy. The approach is useful for understanding
image compression and anomaly detection in medical imaging.

## Technologies Used
- Python
- PyTorch
- OpenCV
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
