🧠 Project Title: Alzheimer’s Disease Detection Using CNN
This project involves designing and training a deep learning model that can accurately detect the stage of Alzheimer’s disease by analyzing MRI brain scans. The goal was to use Convolutional Neural Networks (CNNs) to perform this classification task and build a simple web-based tool so that predictions can be made easily in real time.

The system was developed in Python, with the backend built using Flask and the model trained using TensorFlow and Keras. The final result is a web application that takes an image of an MRI scan and predicts whether the patient is non-demented or in one of the dementia stages: very mild, mild, or moderate.

📁 Dataset Information
The dataset used for training was obtained from Kaggle under the name ImagesOasis - Brain MRI Dataset [Visit Kaggle Dataset](https://www.kaggle.com/datasets/ninadaithal/imagesoasis)
. It includes brain MRI images already sorted into four categories:

Non-Demented

Very Mild Dementia

Mild Dementia

Moderate Dementia

Each category has its own folder of images. Before training, the images were resized to 224x224 pixels and normalized so the model could learn better and faster.

🧠 Model Structure (CNN)
The CNN used in this project includes three main convolutional layers that extract features from the MRI images. Each layer is followed by a pooling layer that reduces the size of the image data, helping the model generalize better.

After flattening the output, it is passed through a fully connected (dense) layer, followed by a dropout layer to prevent overfitting. The final output layer uses softmax to predict one of the four Alzheimer’s categories.

Key configuration:

Image Input Shape: 224x224 pixels (3 color channels)

Training Epochs: 10

Batch Size: 32

Optimizer: Adam

Loss Function: Categorical Crossentropy

✅ Final Results
The model performed extremely well on the test data:

Test Accuracy: 99.95%

Test Loss: 0.0024

📊 Classification Breakdown:

Alzheimer’s Stage | Precision | Recall | F1-Score | Samples
Mild Dementia | 1.00 | 1.00 | 1.00 | 1000
Moderate Dementia | 1.00 | 0.99 | 0.99 | 98
Non-Demented | 1.00 | 1.00 | 1.00 | 13445
Very Mild Dementia | 1.00 | 1.00 | 1.00 | 2745

These results show that the model learned the features very effectively, achieving almost perfect scores on all metrics



