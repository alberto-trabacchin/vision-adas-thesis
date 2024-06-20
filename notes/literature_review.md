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


# VAD Datasets
## 1. Surveillance Cameras (prohib. objects, abnormal movements)
### Anomaly Detection and Localization in Crowded Scenes

Link: https://ieeexplore.ieee.org/document/6531615

### Abnormal Event Detection at 150 FPS in MATLAB

Link: https://ieeexplore.ieee.org/document/6751449

### Future Frame Prediction for Anomaly Detection -- A New Baseline

Prediction of future frame given past frames.

Link: https://arxiv.org/abs/1712.09867


### Real-world Anomaly Detection in Surveillance Videos

Scenes of accidents, robbery, and theft.

Link: https://arxiv.org/abs/1801.04264

## 2. Egocentric Traffic Videos

### Anticipating Accidents in Dashcam Videos

620 videos of road accidents taken from dashcams. Last 10 frames of each video 
are labelled as anomalous.

Link: https://link.springer.com/chapter/10.1007/978-3-319-54190-7_9

### Unsupervised Traffic Accident Detection in First-Person Videos

1,500 anomalous videos with start and end frames' annotations.

Link: https://arxiv.org/abs/1903.00618

### DADA: Driver Attention Prediction in Driving Accident Scenarios

2,000 videos for driver attention (gaze) prediction in accidents. 

Link: https://arxiv.org/abs/1912.12148

Link: https://arxiv.org/abs/1904.12634

### Predicting the Driver’s Focus of Attention: the DR(eye)VE Project
74 videos, 500,000 frames, 6 hrs. total, (RT camera + ETG camera) to predict driver's gaze.

Link: https://arxiv.org/abs/1705.03854

### BDD-A: Predicting Driver Attention in Critical Situations

1,232 (3.5 hrs. total) critical scenes taken from BDD100k.


Link: https://arxiv.org/abs/1711.06406

### Spatio-Temporal Action Graph Networks

Extract a collision dataset with 803 videos from BDD100K.
They do activity recognition.

Link: https://arxiv.org/abs/1812.01233


# VAD Models

## 3. Convolutional Autoencoder (ConvAE)

### Learning Temporal Regularity in Video Sequences

They train ConvAE to reconstruct a sliding window of frames (not prediction).
If the reconstruction loss in high, there is an anomaly.

Link: https://arxiv.org/abs/1604.04574


## 2. Convolutional LSTM Auto-Encoder (ConvLSTMAE)

### Anomaly Detection in Video Using Predictive Convolutional Long Short-Term Memory Networks

Predict the evolution of a video sequence from a small number of input frames.

Link: https://arxiv.org/abs/1612.00390

### Abnormal Event Detection in Videos using Spatiotemporal Autoencoder

Reconstruct a video sequence.

Link: https://arxiv.org/abs/1701.01546

### Remembering history with convolutional LSTM for anomaly detection

Reconstruct a video sequence.

Link: https://ieeexplore.ieee.org/document/8019325

## 3. Others

Is it possible to combine AE (unsupervised) with semi-supervised learning?

Teacher could generate pseudo-labels from labelled data and AE?

Or AE could be trained unsupervised, and fine-tuned on labelled data?