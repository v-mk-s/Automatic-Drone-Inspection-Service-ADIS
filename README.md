# Automatic Drone Inspection Service (ADIS)
🤖DL Research

## Description

I am developing a high-tech automated inspection system for conveyor belts for large mining enterprises (Norilsk Nickel, Polymetal, Evraz). We remove the human factor and reduce the loss of conveyor transport and conveyor downtime. If the conveyor is damaged by a roller that is out of order, the belt breaks and it takes a day to replace it, so the conveyor does not work and its idleness costs a lot. The main idea is to use a neural network based on YOLOv5. We use high-tech equipment for capturing the conveyor: a drone with a dual camera (RGB & IR), an RTK module to track the precise positioning of the drone, complex mathematics to determine the GPS coordinates of broken rollers, and other modern technologies.

## Stack (work in progress)
Python, [YOLOv5](https://github.com/ultralytics/yolov5), [Detectron2](https://github.com/facebookresearch/detectron2), OpenCV, Django

## Results
Developed an object detection & tracking system with an accuracy of 98% by improving YOLOv5 with stack 
input and RGB & IR cameras, leading to increase accuracy to an additional  5%. 

![alt text](https://github.com/v-mk-s/ADIS/blob/master/ADIS-Video-test-15-sec.gif "")

**In yellow [bounding boxes](https://albumentations.ai/docs/examples/example_bboxes/) are broken idlers**

![IR detection](https://github.com/v-mk-s/Automatic-Drone-Inspection-Service-ADIS/blob/master/images/final_result.jpg)


## Work in progress
The source code cannot be presented.

© ADIS 2022
