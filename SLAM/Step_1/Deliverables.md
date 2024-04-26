## Monocular Visual Simultaneous Localization and Mapping by MATLAB

MATLAB has an example of Monocular Visual SLAM linked [here](https://www.mathworks.com/help/vision/ug/monocular-visual-simultaneous-localization-and-mapping.html). A summary of how the example works is in the [README](https://github.com/frankzachma/Visual-Mono-SLAM/blob/main/README.md).

The relevant results of this example from running it on my personal computer are the two pictures below. The first one (top) is the picture with the key points. The second one (bottom) is the optimized trajectory of the camera overlayed with the ground truth trajectory.

![Refine and Visualize the Initial Reconstruction](https://github.com/frankzachma/Visual-Mono-SLAM/assets/168232333/eec3bc35-37a0-4c3a-abfa-ab82af74b2ba)

![Point Cloud Player](https://github.com/frankzachma/Visual-Mono-SLAM/assets/168232333/51d9f0e4-cac9-4e9b-8584-250536f6f5f0)


This type of application can be used for the digital reconstruction of a building such that the user can estimate if an object(s) can fit inside of a given space. This can also be done to recreate 3-D geometries for the use inside of 3-D models. One can also track the motion of the camera using monocular visual SLAM and verify the path if the camera parameters are known. This can be done with the example from MATLAB but with a few minor tweaks to the code to adjust for your dataset file types. To fully use the MATLAB example, one must also find the camera parameters to ensure the use of the ground truth part of the code.
