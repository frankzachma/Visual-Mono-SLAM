## Monocular Visual Simultaneous Localization and Mapping by MATLAB Using Custom Dataset

MATLAB has an example of Monocular Visual SLAM linked [here](https://www.mathworks.com/help/vision/ug/monocular-visual-simultaneous-localization-and-mapping.html). However, in order to achieve the same results as done by MATLAB, a few edits must be made to the code. Below shows the only added code. All of changes to MATLAB's example was done to the "Download and Explore the Input Image Sequence." The reason this is the only neccessary place to change anything is because the dataset file type is much different. The dataset I used was individual pictures in a folder on my computer. MATLAB had us download files and extract them based on the type of file that was downloaded. So, all of the first block of code in this section was commented out. The second block was changed to the code below. 
````
imageFolder   = fullfile('C:\Users\fzachma\Documents\Visual SLAM Project\Pictures');
imds          = imageDatastore(imageFolder);

% Inspect the first image
currFrameIdx = 1;
currI = readimage(imds, currFrameIdx);
himage = imshow(currI);
````


Now that the only neccessary changes have been made, the results of each section of the MATLAB blocks code that are relavent are shown below.

*Map Initialization Result*
![image](https://github.com/frankzachma/Visual-Mono-SLAM/assets/168232333/ff944739-1833-46e8-826b-c441c35cc3bb)

*Refine and Visualize the Initial Reconstruction Result 1*
![image](https://github.com/frankzachma/Visual-Mono-SLAM/assets/168232333/4af6c376-86a3-4c6a-a0b5-262a07d4b3c0)

*Refine and Visualize the Initial Reconstruction Result 2*
![image](https://github.com/frankzachma/Visual-Mono-SLAM/assets/168232333/04c6c05c-7fa3-44bc-bb72-6a80fa8b5ffd)

*Loop Closure Result 1*
![image](https://github.com/frankzachma/Visual-Mono-SLAM/assets/168232333/e5e7b16e-9e6a-4028-9682-833c7923a310)

*Loop Closure Result 2*

![image](https://github.com/frankzachma/Visual-Mono-SLAM/assets/168232333/8f5db104-bac8-4f3c-b0ca-2501f95325d5)


These results are the reconstructed scene from the images and predicted camera trajectory. The camera parameters were not aquired, so the ground truth trajectory was not part of the results.
