# FCAV M-Air Pedestrian (FMP) Dataset
This repository includes a link to FCAV M-Air Pedestrian (FMP) Dataset. A small dataset along with videos are provided in this repository as an example. To download the full dataset, please use the link below. The dataset contains monocular RGB images and Planar LiDAR data for pedestrian detection. Videos are also included in this link.

[Download full dataset here](https://drive.google.com/open?id=1vBk0fDZRf3Tq3Wauwry4OiminLXkv7Q-)

The FMP dataset was collected from an HD camera and a Hokuyo UTM-30LX-EW planar LiDAR mounted on a ROS-enabled Segway mobile robot platform. The dataset was collected in an outdoor environment using the "M-Air" facility at the University of Michigan campus in Ann Arbor, MI, USA in January 2019. A Qualisys Motion Capture system was used to record shoulder key-points of pedestrians for ground truth data.

The FMP dataset contains four short videos with a total recording time of about 4 minutes and we used 3,934 frames with good quality ground truth. In each frame, there are up to two pedestrians walking in the scene, interacting with and sometimes occluding each other. 

Currently this dataset folder structure and format are arranged as [KITTI's](http://www.cvlibs.net/datasets/kitti/). Four txt files that contains sample sequence numbers are given as examples for training, validation, and testing. Specifically, the last video clip (810 frames) was selected as the test set. Frames from the remaining three sequences (3,124 frames) are randomly shuffled for training and validation with 3:1 ratio.

```
Kitti
└── object
    ├── training
    │   ├── calib
    │   │   ├── xxxxxx.txt
    │   │   └── xxxxxx.txt
    │   ├── rgb_images
    │   │   ├── xxxxxx.jpg
    │   │   └── xxxxxx.jpg
    │   ├── label_2
    │   │   ├── xxxxxx.txt
    │   │   └── xxxxxx.txt
    │   ├── planes
    │   │   ├── xxxxxx.txt
    │   │   └── xxxxxx.txt
    │   └── planar_lidar_ptclouds
    │       ├── xxxxxx.ply
    │       └── xxxxxx.ply
    ├── train.txt
    └── val.txt
    └── test.txt
```

![](media\1_pedestrian.gif)


**Projects that use this dataset (as of Nov. 2019)**

Pedestrian Planar LiDAR Pose (PPLP) Network for Oriented Pedestrian Detection Based on Planar LiDAR and Monocular Images, Fan Bu, Trinh Le, Xiaoxiao Du, Ram Vasudevan, and Matthew Johnson-Roberson

