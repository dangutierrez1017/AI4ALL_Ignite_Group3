# Enhancing Nutrition Tracking Through Image Classification

Develop a model in PyTorch that will be trained on a food image dataset for classification.


## Essential Question <!--- do not change this line -->

Q: How can the process of creating AI/ML solutions amplify or mitigate bias in the case our team is using?

A: Through fine tuning an existing ML model using multiple random samples of datasets, we can mitigate potential bias prevalent in existing datasets. 

## Key Results <!--- do not change this line -->

In order to establish a baseline, the model was trained on the training set and subsequently validated on the test set for 5 concurrent epochs, where we then recorded the model’s performance during that run
Although we saw a steady decline in validation loss during this run, we immediately noticed a plateau in the training loss
We ended the run with a Top-5 Accuracy of 4.93% and a Top-1 Accuracy of 1.07%
Along with the previous metrics, the nearly zero’d out confusion matrix that showed a large number of false negatives indicated that there was significant overfitting. This is either due to Resnet-50’s complexity, not large enough dataset, or the effects of pretrained weights onto the model’s generalization.

We attempted to address the issue of overfitting and incredibly low accuracy in the next two runs by fine-tuning our model though a range of techniques. These included
- L1 Regularization 
- Early Stopping 
- Layer Freezing
- Learning Rate Decay Scheduler
  
We also wanted a way to a increase the size of the training set( in case it was not large enough) by performing different image augmentations on the test set to feed into each run of the training/testing loops. Some included
- Random Horizontal Flips
- Blurring
- Discoloration




## Methodologies <!--- do not change this line -->

Convolutional Neural Network - Deep Learning (Resnet-50)
- *Stems from Torch’s AI framework*
- *Supervised to be able to classify images*
  
Converted our input testing images using the Python library Pytorch
- *Resized and converted into Tensor 3D objects*
  
Inputted image of food, received confidence percentage of inputted image and name




## Data Sources <!--- do not change this line -->

Datasets: [Link to Kaggle Dataset](https://www.kaggle.com/datasets/kmader/food41)

## Technologies Used <!--- do not change this line -->

- *Python*
- *Kaggle Notebooks*
- *Google Colabs*
- *Pytorch*
- *Seaborne*
- *Scikit-learn*
- *Pandas*
- *MatPlotLib*


## Authors <!--- do not change this line -->

*This project was completed in collaboration with:*
- *Lucy Wang ([lw3501@princeton.edu](mailto:lw3501@princeton.edu))*
- *Wenjia Song ([wenjia@berkeley.edu](mailto:wenjia@berkeley.edu))*
- *Oluwadayo Bamgbelu ([dayob@tamu.edu](mailto:dayob@tamu.edu))*
- *Daniel Gutierrez ([dguti124@fiu.edu](mailto:dguti124@fiu.edu))*
