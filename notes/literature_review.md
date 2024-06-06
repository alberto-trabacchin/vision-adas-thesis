# Literature Review

## 1. Computer Vision based Accident Detection for Autonomous Vehicles

### Link: http://www.arxiv.org/pdf/2012.10870

### Description:
Detection of car accidents in driving scenarios downloaded from YouTube.
They track all the vehicles and use an accident detection policy depending on:

1. Two bboxes are in part overlapping on both axes
2. The bboxes are on the same lane section
3. Acceleration anomaly
4. Trajectory anomaly
5. Change in angle anomaly

### Pros:
1. System more robust to specific scenarios (highways).

### Cons:
1. They not consider all many possible scenarios (road lanes)
2. No specific info on dataset
3. No specific values of alpha, beta, gamma and threshold
4. No code provided


## 2. DoTA Dataset

### Link: https://arxiv.org/pdf/2004.03044

### Description:
They use a **What, When, Where** pipeline to detect **What** kind of accident 
happened, **When** it happened and **Where** it happened.
They made experiments in supervised and unsupervised learning modes.

Unsupervised:

1. Convolutional Autoencoder (reconstructs next frame)
2. Convolutional LSTM Autoencoder (CNN + LSTM, takes multiple frames)
3. AnoPred (predicts future frames and uses other features, see 3.)

Supervised:




### Pros:
1. Dataset with 4,677 annotated videos.
2. Data and code provided.

### Cons:
1. 


## 3. Future Frame Prediction for Anomaly Detection – A New Baseline

### Link: https://arxiv.org/pdf/2004.03044 (CVPR-2018)

### Description:
Model used to predict future frames depending on multiple features, such as:

1. Image frames
2. Optical flow
3. Gradient
4. Adversarial loss

### Pros:
1. Code provided
2. Tested on multiple datasets

### Cons:
1. Not tested on driving scenarios