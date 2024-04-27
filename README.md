# Visual-Monocular-SLAM-Project
## Document Overview
The following GitHub repository is a collection of details about visual monocular simultaneous localization and mapping. The original code is completed and installed as an example by MATLAB themselves, which is referenced [here](https://github.com/frankzachma/Visual-Mono-SLAM/blob/main/SLAM/Step_2/Deliverables.md). In order for the code to work for a custom dataset, there were edits made to the code, which is discussed in detail [here](https://github.com/frankzachma/Visual-Mono-SLAM/blob/main/SLAM/Step_2/Deliverables.md). The custom [dataset](https://github.com/frankzachma/Visual-Mono-SLAM/tree/main/SLAM/Step_2/Pictures) in questions contains pictures taken of a classroom lectern using a laptop camera. 

## Summary of MATLAB's Visual Monocular SLAM using ORB-SLAM
The monocular visual simultaneous localization and mapping example from MATLAB shows a visual SLAM system using monocular camera images. This example combines feature detection, feature matching, pose estimation, and map generation to build a point cloud map of the environment.

The camera parameters, specifically the intrinsic camera parameters, are used to estimate the relative rotation and translation between the first two images of the dataset to establish a baseline. Along with these parameters, the map initialization block of code generates features for both pictures and then matches the features that are the same in both pictures. Oriented FAST and rotated BRIEF (ORB) is the feature detection algorithm that is used to pick out various feature points. If the scene is planar, the homography projective transformation is used to describe the motion between frames using features that match. If the scene is not planar, the fundamental matrix is used instead. Once the camera motion is estimated, 3-D points corresponding to the matched features are triangulated and inserted into the 3-D point cloud. This process estimates the depth of each feature point by using the known camera pose constructed from the camera's intrinsic parameters. Loop closure is used to determine when the camera has come back to the same location. This helps to correct for accumulated drift and refines the map. 

A comparison to the ground truth data can be made using the generated point cloud map. The ground truth data is generated using recorded datasets with known camera poses and scene geometry. This comparison is important for understanding the accuracy and performance of the SLAM system. This is useful for quantifying pose estimation error, map accuracy, and loop closure detection rate.

## Monocular Visual SLAM Implementation
This type of application can be used for the digital reconstruction of a building such that the user can estimate if an object(s) can fit inside a given space. This can also be done to recreate 3-D geometries for the use inside of 3-D models. One can also track the motion of the camera using monocular visual SLAM and verify the path if the camera parameters are known. This can be done with the example from MATLAB but with a few minor tweaks to the code to adjust for your dataset file types. To fully use the MATLAB example, one must also find the camera parameters to ensure the use of the ground truth part of the code.
