# Visual-Monocular-SLAM-Project
Summary







![image](https://github.com/frankzachma/Visual-Mono-SLAM/assets/168232333/5bb5e1fc-f943-4e67-bc9b-2da9b39b1daf)


![image](https://github.com/frankzachma/Visual-Mono-SLAM/assets/168232333/ff944739-1833-46e8-826b-c441c35cc3bb)


![image](https://github.com/frankzachma/Visual-Mono-SLAM/assets/168232333/4af6c376-86a3-4c6a-a0b5-262a07d4b3c0)


![image](https://github.com/frankzachma/Visual-Mono-SLAM/assets/168232333/04c6c05c-7fa3-44bc-bb72-6a80fa8b5ffd)


![image](https://github.com/frankzachma/Visual-Mono-SLAM/assets/168232333/e5e7b16e-9e6a-4028-9682-833c7923a310)


![image](https://github.com/frankzachma/Visual-Mono-SLAM/assets/168232333/8f5db104-bac8-4f3c-b0ca-2501f95325d5)

````
imageFolder   = fullfile('C:\Users\fzachma\Documents\Visual SLAM Project\Pictures');
imds          = imageDatastore(imageFolder);
% Inspect the first image
currFrameIdx = 1;
currI = readimage(imds, currFrameIdx);
himage = imshow(currI);
````
