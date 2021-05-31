---
layout: post
title: What is Caffe Framework.
subtitle: Deep learning Framework.
tags: [MACHINE_LEARNING, data-science]
image: /img/caffe2.png
comments: true
---
![Life](/img/caffe.png)
**What is deep learning?**

**Deep learning** is a part of **Machine Learning** methods and techniques based on learning data patterns and making predictions. The learning in this case, by an ML model, can be supervised, semi-supervised or unsupervised. In Deep learning we are actually trying to mimic the human brain inside the computer. Deep learning algorithms are inspired by and based on the human brain&#39;s structure and function, and are called **Artificial Neural Networks**.

**What actually is Caffe???**

**Caffe** is a deep learning framework characterized by its speed, scalability, and modularity. Caffe works with CPUs and GPUs and is scalable across multiple processors. This Deep Learning Framework is suitable for industrial applications in the fields of computer vision, Natural language processing and other multimedia such as audio and video.

**Why is Caffe a popular choice for Deep Learning?**

Caffe has been designed for the purposes of fast training, open-source development, narrative architecture and seamless community support. All these features make Caffe framework a famous choice for designing Deep Learning models.

- **Flexible Code: ** The Caffe framework features top-notch codes, algorithms and models. Over the time, Caffe has seen many changes contributed by the developers and researchers around the globe which makes it a great platform for deep learning projects.
- **Narrative architecture**** : **A narrative and modular architecture of Caffe allows for enhanced development of applications and programs on machine learning. We can define the models and optimize them without any efforts. We can switch between GPU (Graphics Processing Unit) and CPU by using a single-flag and train the ML model on a GPU machine. The model can be then deployed any platform.
- **Speed: ** The most important feature that makes Caffe a famous choice for Deep Learning operations. With a single Nvidia K40 GPU, Caffe can process over 60 million images per day. That speed translates to 1 millisecond/image for inference and 4 milliseconds/image for learning operations. Recent library versions and latest hardware are still boosting Caffe&#39;s speed performance. This makes Caffe framework a perfect candidate for deploying deep learning ML models at industry level as well as for research experiments.
- **Community support: ** The users of Caffe platform can get developer support from Caffe-users group and GitHub platform. Various startup-prototypes, academic research projects, and industrial applications relating to vision, speech, and multimedia recognition have been forged on Caffe, and powered by the support of Caffe Community.

**How caffe works?**

- Caffe stores and process data in so called **Blobs**.
- A blob is a standard array and unified memory interface.
- The properties of blob describe how information is stored in various layers of neural network and how it is communicated across the network

**How is blob stored and communicated?**

- A blob is a wrapper over the actual data being processed and passed along by caffe.
- And also under the hood provides the synchronization capacity between CPU and GPU.
- Mathematically, a Blob is an N dimensional array stored in continuous fashion.
- The conventional blob dimensions for batches of image data are:

Number (N) \* Channel (K) \* Height (H) \* Width (W)

Where:

Number = Batch size of the Data.

Channel = Feature dimension.(for RGB images K = 3)

![Life](/img/caffe3.png)

**Steps in training Caffe model.**

1. Data preparation.
2. Model definition: In this step we choose CNN architecture and we define its parameters in a config file with extension .prototxt.
3. Solver definition: Th solver is responsible for model optimization. We define solver parameters in a config with extension .prototxt.
4. Model training: we train the model by executing one caffe command from terminal. After training the model, we will get the trained model in a file extension .caffemodel.
