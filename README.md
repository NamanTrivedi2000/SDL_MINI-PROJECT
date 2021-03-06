# FaceMaskDetection

## We have used open source all the popular deep learning framework' model and inference code to do face mask detection.
 + Keras
 
 
 
 ** Detect faces and determine whether they are wearing mask.**

** First of all, we hope the people in the world defeat COVID-2019 as soon as possible. Stay strong, all the countries in the world.**

+ We make face mask detection models with five mainstream deep learning frameworks （PyTorch、TensorFlow、Keras、MXNet,Caffe） open sourced, and the corresponding inference codes.

![alt text](https://res.cloudinary.com/practicaldev/image/fetch/s--1u3Uz9sp--/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://dev-to-uploads.s3.amazonaws.com/i/ojmek5e5tihf1p655ju6.png)

## MODEL STRUCTURE

We used the structure of SSD. However, in order to make it run quickly in the browser, the backbone network is lite. The total model only has 1.01M parametes.

Input size of the model is 260x260, the backbone network only has 8 conv layers. The total model has only 24 layers with the location and classification layers counted.

SSD anchor configurtion is show bellow:

|Multibox layers| feature map size| anchor size | aspect ratio|
|---------------|-----------------|--------------|-------------|
|First	         |33x33            |	0.04,0.056  |	1,0.62,0.42  |
|Second		       |17x17            |	0.08,0.11   |               |
|Third	         |9x9	             |0.16,0.22	    |1,0.62,0.42|
|Forth	         |5x5	             |0.32,0.45      |	1,0.62,0.42|
|Fifth	         |3x3	             |0.64,0.72	      |1,0.62,0.42|

## HOW TO RUN

## Keras

on image：

``` python
python keras_infer.py  --img-path /path/to/your/img
```
on video：

```python
python keras_infer.py --img-mode 0 --video-path /path/to/video  
# If you want to run with camera video, set  video_path to be 0
python keras_infer.py --img-mode 0 --video-path 0
```

