
# CycleGAN Project

## Overview

This repository contains the code and results of the CycleGAN project. The main goal of this project was to apply CycleGAN (Cycle-Consistent Generative Adversarial Networks) for generating images, particularly focusing on the faces of cats, dogs, and Marvel Heroes.

CycleGAN is a type of generative adversarial network (GAN) designed for image-to-image translation tasks where paired examples are not available. The model was utilized to translate between various datasets without the need for paired images.

## Data Processing

- **Datasets Used**: 
  - Faces of cats, dogs, and people were extracted for the project.
  - The data was preprocessed using Python libraries such as `zipfile`, `os`, and `shutil`.
  
- **Data Split**:
  - For the cat and dog datasets, a 70:30 train-test split was applied.
  - Images were loaded using the directory-based image dataset method, excluding explicit labels due to the nature of the CycleGAN task.

## Model

- **Modeling Approach**: 
  - The project utilized transfer learning with a pre-trained CycleGAN model.
  - The model was trained for 50 epochs to generate images that resemble cat or dog faces.
  
- **Additional Experiment**: 
  - The model was later fine-tuned and run on a new dataset consisting of images of Marvel Heroes to generate interesting cross-domain image translations.

## Results

The generated images for both the cat/dog datasets and the Marvel Heroes dataset were visualized in the notebook. The results showed the model's ability to generate high-quality, realistic images that translated well between the domains.

## Steps to Execute this Project

**NOTE**: Running the whole project might take an extended period of time. Training time also depends on your system's computational capabilities.

1. **Download the project**:
   - Unzip the folder provided.
   - Download the image dataset separately and upload it to your Google Drive in the following paths:
     ```bash
     dog_zip_path = '/content/drive/MyDrive/GAN/cat_and_dog/dog faces.zip'
     cat_zip_path = '/content/drive/MyDrive/GAN/cat_and_dog/cat_face.zip'
     face_crop1 = '/content/drive/MyDrive/GAN/face_img/UTK Face Cropped.zip'
     face_crop2 = '/content/drive/MyDrive/GAN/face_img/face_align_celeba.zip'
     ```

2. **Model Evaluation**:
   - If you want to see how the model works without retraining, load the pre-trained model included in the project.
   - Navigate to the "Model Evaluation" section of the notebook and run the cells under that section.

3. **Modifying the Code**:
   - Before running the code, you may want to comment out some models (if multiple models are applied) containing the command `model.fit` to avoid unnecessary retraining.

4. **Predicted Output**:
   - The folder `output`, containing predicted images, is attached in the project zip file.

## Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/CycleGAN.git
   ```

2. Navigate to the project directory and install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the notebook to train or generate images:
   ```bash
   jupyter notebook CycleGAN.ipynb
   ```

4. Replace datasets as needed for your own experiments, ensuring the directory structure follows the format in the notebook.

## Requirements

- Python 3.x
- TensorFlow
- Keras
- Zipfile, os, shutil libraries

## Authors

- Rohit Kumar (C2052473)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
