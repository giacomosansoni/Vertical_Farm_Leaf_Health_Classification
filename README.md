# Deep Learning for Vertical Farm Leaf Health Classification

The aim is to classify images of plants into healthy and unhealthy categories using CNNs

## Dataset

The dataset used for this project can be found [here](https://drive.google.com/file/d/1llWCmIbaW-uHvZcD-soT8DJQJYmm8zAA/view?usp=drive_link).

## Data Preprocessing

The dataset initially consisted of 5200 96x96 RGB images, categorized into healthy and unhealthy leaves. Outliers were identified and removed, resulting in a refined dataset of 4850 images. To tackle class imbalance, data augmentation was applied (flip and rotation).

## Training

### Transfer Learning

Various VGG16 pre-trained architectures were evaluated.

### Fine-Tuning

The pre-trained model was fine-tuned by progressively unfreezing the the convolutional network. This process significantly improved accuracy on the validation set with respect to transfer learning only.

## Ensemble

The effectiveness of combining multiple architectures was studied (VGG16 and MobileNet structures). Noticing that averaging the outputs was not performing well, the concatenation of these outputs and the introduction of additional layers (a dense output layer employing softmax activation) achieved commendable validation accuracy without succumbing to overfitting.


## Files in the Repository

- **.gitattributes:** Git attributes file.
- **DataExploration.ipynb:** Jupyter Notebook containing code for data cleaning and preprocessing, including the removal of outliers and duplicates.
- **VGG16 and Resnet50.ipynb:** Jupyter Notebook demonstrating the data augmentation and finetuning of VGG16 and Resnet50.
- **FinalModel_Ensemble.ipynb:** Jupyter Notebook showing the final ensemble model.
- **README.md:** Project's README file providing an overview and documentation.
- **report.pdf:** Detailed report outlining the project's workflow, methodologies, and results.

