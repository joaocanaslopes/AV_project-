Project Proposal

Plant Disease Classification using Transfer Learning

Due Date: 30th of June 2026

Team Members: João Lopes (24842) & Lourenço Carvalho (29248)

### 1. Problem Statement

Plant diseases have a devastating impact on agricultural yield, causing significant economic losses and threatening global food security. Early, accurate, and rapid detection of these diseases is crucial to mitigate their spread. Traditionally, disease identification requires manual inspection by domain experts, which is time-consuming, expensive, and prone to human error. This project investigates how computer vision can automate this process. It is a highly interesting problem because it bridges the gap between advanced deep learning techniques and real-world agricultural challenges, potentially empowering farmers with accessible and reliable diagnostic tools.

### 2. Challenges

Developing an effective plant disease classification model presents several key challenges:

*   **High Intra-class Variation:** The visual appearance of a single disease can vary drastically depending on the stage of infection, lighting conditions, and the specific plant variety.
*   **Low Inter-class Variation:** Symptoms of different diseases (e.g., various types of leaf spots or blights) can look remarkably similar to the naked eye.
*   **Background Clutter:** While some datasets feature leaves on solid backgrounds, real-world field images contain complex backgrounds, including soil, stems, and other leaves, which can confuse the model's feature extraction.
*   **Class Imbalance:** Readily available datasets may have an unequal distribution of images across different disease classes, potentially leading to biased model predictions.

### 3. Dataset

For this project, we plan to utilize the PlantVillage dataset, a well-established and publicly available dataset widely used in agricultural computer vision research. It contains tens of thousands of high-resolution images of healthy and diseased crop leaves across various species (such as apple, corn, potato, and tomato). We will gather this dataset from an online data repository, specifically Kaggle. If necessary to improve robustness, we may augment this dataset with additional real-world field images sourced from other open agricultural databases.

### 4. Method or Algorithm

We propose to use **Transfer Learning** with pre-trained Convolutional Neural Networks (CNNs). Training a deep neural network from scratch requires massive amounts of data and computational power. By leveraging models that have been pre-trained on large-scale datasets (like ImageNet), we can transfer their learned feature extraction capabilities to our specific agricultural problem. Specifically, we plan to fine-tune state-of-the-art architectures such as **ResNet50** and **MobileNetV2**. The lower layers of these models will recognize fundamental features (edges, textures), while we will retrain the final fully connected layers to classify our specific plant diseases.

### 5. Evaluation

To rigorously evaluate our results, we will split the dataset into training, validation, and testing sets. Our analysis will rely on the following evaluation strategies:

*   **Performance Metrics:** We will measure overall Accuracy, as well as Precision, Recall, and the F1-Score, which are crucial for understanding the model's performance across potentially imbalanced classes.
*   **Confusion Matrix:** This will be used to visualize misclassifications and identify which specific diseases the model struggles to differentiate.
*   **Comparative Analysis:** We will compare the performance of at least two different architectures (e.g., the deeper ResNet50 versus the lightweight MobileNetV2). The comparison will focus on both classification accuracy and inference time, which is a critical factor for potential deployment on mobile devices for field use.
