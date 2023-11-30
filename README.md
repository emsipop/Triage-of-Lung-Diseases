# Self-Supervised Deep Learning for Triage of Lung Diseases from X-Rays
## Overview
Triage can be challenging to maintain across the healthcare sector when it comes to prioritising treatment for the most vulnerable patients. With the COVID-19 pandemic as an obstacle, it is easy to prioritise this and overlook those with other life-threatening diseases who may require treatment more urgently. This project aims to address this issue by leveraging self-supervised deep learning on X-rays, providing a comprehensive solution for triage in lung diseases.

## Motivation
In the backdrop of the COVID-19 pandemic, it has become crucial to reassess and improve the triage process. This project incorporates a review of previous academic research, the development of a solution, and an evaluation of the obtained results to enhance the medical and ethical reliability of triage. By investigating self-supervised deep learning on X-rays, the project seeks to contribute to the efficient and accurate prioritisation of patients.

## Objectives
* Solution Development: Implementation of self-supervised deep learning on X-rays with a focus on developing two pretext tasks. These tasks aid in the creation of a downstream task aimed at diagnosing lung diseases in patients.

* Result Evaluation: Comprehensive evaluation of obtained results to assess the effectiveness of the proposed solution. High accuracies, reaching up to 0.9336, were achieved when utilising the pretext tasks for pre-training, indicating the potential for successful triage implementation in the future.

* Resource-Efficient Models: Demonstration that self-supervised deep learning can enhance model accuracy even in environments with limited resources, showcasing the practicality and adaptability of the approach.

## Features
* Self-supervised learning: The model is trained in a self-supervised manner, minimising the need for annotated data.

* Deep neural network architecture: Utilises state-of-the-art deep learning architectures tailored for medical image analysis.

* Triage capability: The model can triage X-ray scans based on detected lung diseases, aiding in prioritising critical cases.

## Results
### Pretext Task 1: Rotation Classification
The first pretext task involved classifying the rotation in degrees (0, 90, 180, and 270) that has been applied to an image.

<img src="https://github.com/emsipop/Triage-of-Lung-Diseases/assets/60201307/469e842f-f245-4eea-b834-d937db6261a9" width="150"/>
<img src="https://github.com/emsipop/Triage-of-Lung-Diseases/assets/60201307/877e2287-6eb8-4572-9f59-ac24731972fd" width="150"/>
<img src="https://github.com/emsipop/Triage-of-Lung-Diseases/assets/60201307/d7419816-efe1-448d-9c38-f8b0b1c0ec9f" width="150"/>
<img src="https://github.com/emsipop/Triage-of-Lung-Diseases/assets/60201307/b3e948b4-ef24-4d3c-89e4-8e24677b994b" width="150"/>

* Test Accuracy: 100%

### Pretext Task 2: Grid Location Classification
A similar process was undertaken for the second pretext task, which involved classifying the position of a section of an image in a 2x2 grid.

<img src="https://github.com/emsipop/Triage-of-Lung-Diseases/assets/60201307/fc09132a-17ca-40dc-b7f6-d7eafe51139e" width="200"/>

* Test Accuracy: 97.36%

### Downstream Task: Lung Disease Classification
The downstream task involves training a deep learning model to classify X-ray images based on the presence of lung diseases. The primary goal is to accurately identify and categorise images into different classes representing specific lung conditions, such as COVID-19, Tuberculosis (TB), and normal (no disease). The model's training is focused on learning the intricate patterns and features within the X-ray images that distinguish between various lung diseases.

<img src="https://github.com/emsipop/Triage-of-Lung-Diseases/assets/60201307/a29aaf41-0a68-482f-818d-8dcd5541d213" height="150"/>
<img src="https://github.com/emsipop/Triage-of-Lung-Diseases/assets/60201307/8a85714f-2767-4420-b06f-aeb3cc6020e6" height="150"/>
<img src="https://github.com/emsipop/Triage-of-Lung-Diseases/assets/60201307/00469b35-12df-4597-b634-a4c545267490" height="150"/>
<img src="https://github.com/emsipop/Triage-of-Lung-Diseases/assets/60201307/dd3b76a8-bd85-4685-bc5f-b09a8fbc6e55" height="150"/>

* Without Pre-training: 86.71%
* Pre-training with Task 1: 93.36%
* Pre-training with Task 2: 91.36%

### Image Quality and Availability
* Dataset Size Impact: Increasing images decreased test accuracy but still improved with pre-training.
* Gaussian Blur Experiment: Test accuracy decreased with blur but still higher with pre-training.

## Conclusion
* Pre-training Impact: Both pretext tasks significantly improve downstream task accuracy.
* Resource Considerations: Task 1 is more efficient and computationally economical.
* Potential for Limited Resources: Pre-training still beneficial even with smaller datasets and poor image quality.
