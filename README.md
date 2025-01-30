### README for Summer2Winter CycleGANs

#### Introduction
This repository contains a CycleGAN implementation for translating images between summer and winter seasons using PyTorch. The model architecture includes generators and discriminators for both directions of translation (summer to winter and winter to summer).

#### Installation
1. Clone the repository:
   ```
   git clone https://github.com/samay2504/summer2winter_cycleGANs.git
   cd summer2winter_cycleGANs
   ```

2. Install the required dependencies:
   ```
   pip install torch torchvision matplotlib pillow
   ```

#### Dataset
Ensure your dataset is structured as follows:
```
Dataset/
    trainA/
    trainB/
    testA/
    testB/
```
Update the paths in the notebook accordingly.

#### Running the Notebook
1. Open the `code.ipynb` Jupyter Notebook.
2. Follow the cells sequentially to:
   - Load libraries and define classes.
   - Configure device and hyperparameters.
   - Initialize models and optimizers.
   - Define loss functions and schedulers.
   - Create datasets and data loaders.
   - Train the models.
   - Save and test the models.

#### Model Architecture
- **Generator**: Consists of initial convolution, downsampling, residual blocks, and upsampling layers.
- **Discriminator**: Convolutional layers with LeakyReLU activations.

#### Training
The notebook includes a training loop with logging for generator and discriminator losses. Intermediate generated images and models are saved periodically.

#### Testing
The notebook provides a section to load saved models and perform translations on the test dataset. The results are saved in the `results/` directory.

#### Results
Example outputs:
- Original Image (A) - Summer
  ```
  ![summer1](https://github.com/user-attachments/assets/74a89a42-f9b4-41da-95b2-e6d62b1fcbfc)
  ```
- Translated Image (B) - Winter
  ```
  ![winter1](https://github.com/user-attachments/assets/50248bbc-748d-43e6-bb66-41e1349bfffd)
  ```
- Original Image (A) - Winter
  ```
  ![winter2](https://github.com/user-attachments/assets/f9bacf2e-ccd3-43fd-8a71-04b90a2478bd)
  ```
- Translated Image (B) - Summer
  ```
  ![summer2](https://github.com/user-attachments/assets/644ca9e4-ea20-4e08-aaf1-da6892adff4b)
  ```
  
#### Visualization
The notebook plots the training losses of the generator and discriminators.

#### Directory Structure
Use the provided function to print the directory structure of your dataset.

#### Notes
- Ensure the paths to your dataset and models are correctly specified in the notebook.
- Adjust hyperparameters as needed for your specific use case.

For detailed code and implementation, refer to the [code.ipynb](https://github.com/samay2504/summer2winter_cycleGANs/blob/main/code.ipynb) file.
