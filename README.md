# COVID-CXR
The task our model performs is binary classification to predict COVID-19 positive or negative cases based on CXRs. The model takes .jpg or .png image files as input and resizes them to 224x224. After resizing the images, their pixel values are rescaled so they lie in the interval [0, 1]. We also added random horizontal flipping to reduce overfitting during trainining. The model was trained in two steps. First, we pretrained the model on a similar binary classification : normal vs abnormal. By doing so, we familiarized the model with normal CXRs. After pretraining the model on that dataset, we used those weights and fine-tuned our model on Emory’s COVID-19 dataset. In the pretraining step, we used a ResNet50 pretrained on imagenet weights as the base model.

![alt text](https://github.com/Emory-HITI/COVID-CXR/blob/main/image.jpg?raw=true)
![alt text](https://github.com/Emory-HITI/COVID-CXR/blob/main/image.jpg?raw=true)
![alt text](https://github.com/Emory-HITI/COVID-CXR/blob/main/image.jpg?raw=true)
