# The WPC Database
This database was created by Honglei Su (suhonglei@qdu.edu.cn) from University of Waterloo in 2018. We welcome everyone to carry on the test and propose the modification opinion. If you use our database https://drive.google.com/drive/folders/1dHDqKXgvkUhQdUzT7pJjrJ7zRnceFIkO?usp=sharing (a Google account required) in your paper, please cite our papers: 

[1] Honglei Su, Yuxin Liu, Qi Liu et al., Bitstream-based Perceptual Quality Assessment of Compressed 3D Point Clouds, submitted to IEEE Trans. on Image Processing.

@article{su2021bitstream,  
title={Bitstream-based Perceptual Quality Assessment of Compressed 3D Point Clouds},  
author={Su, Honglei and Liu, Yuxin and Liu, Qi and Yuan, Hui and Yang, Huan and Pan, Zhenkuan and Wang, Zhou},  
journal={IEEE Transactions on Image Processing},  
year={2021},  
publisher={IEEE}  
}  

[2] Honglei Su, Zhengfang Duanmu, Wentao Liu et al., Perceptual Quality Assessment of 3D Point Clouds, 2019 IEEE International Conference on Image Processing (ICIP), IEEE, 2019.

@inproceedings{su2019perceptual,  
  title={Perceptual quality assessment of 3D point clouds},  
  author={Su, Honglei and Duanmu, Zhengfang and Liu, Wentao and Liu, Qi and Wang, Zhou},  
  booktitle={2019 IEEE International Conference on Image Processing (ICIP)},  
  pages={3182--3186},  
  year={2019},  
  organization={IEEE}  
}  

Motivated by the lack of source 3D point cloud, we gather acollection of objects with diverse geometric and textural complexity,  including  snacks,  fruits,  vegetables,  office supplies,and containers, etc. The selected contents are moderate in size and are omni-directionally acquirable. The figure and table show snapshots and characteristics of 20 point clouds in the WPC database. **In addition, the WPC database also contains five other point clouds named Coffee_cup, Croissant, Pear, Salt_box and Sweet_potato**.

![image](https://github.com/qdushl/Waterloo-Point-Cloud-Database/blob/main/Snapshots.jpg)
![image](https://github.com/qdushl/Waterloo-Point-Cloud-Database/blob/main/Characteristics.png)

Distortion types and parameter setting:

Downsampling: We apply octree-based downsampling to the normalized point clouds. Each dimension is uniformly divided into 2^N intervals, where N represents the octree level. Then points located in the same cube are merged into one node. In this database, we set N to be 7, 8, and 9, respectively, to cover diverse spatial resolutions.

Gaussian noise: White Gaussian noise is added independently to both geometry and texture elements with standard deviation of {0, 2, 4} and {8, 16, 32}, respectively. Then both geometry and texture elements are rounded to the nearest integer, followed by points removal by Meshlab.

G-PCC (T)/S-PCC: G-PCC (Trisoup) reference codec is employed to encode the original point clouds with ‘max NodeSizeLog2’ of {10}, ‘NodeSizeLog2’ of {2, 4, 6} (‘triSoupLevel’ of {4, 6, 8}) and ‘rahtQuantizationStep’ of {64, 128, 256, 512}, respectively.

V-PCC: V-PCC reference codec is employed to encode the original point clouds at three ‘geometryQP’ values and three ‘textureQP’ values, ranging from 35-50 and 35-50, respectively, followed by duplicated points removal.

G-PCC (O)/L-PCC: It employs downsampling method to encode the geometry information, and is thus not performed redundantly. We set the ‘quantizationSteps’ of texture encoding as {16, 32, 48, 64}.

Subjective test：

We choose passive watching instead of interactive watching for subjective tests because the latter creates large variations and inconsistencies in terms of the viewpoints and viewing time between subjects and viewing sessions. We employ Technicolor renderer to render each point cloud to a video sequence. The rendering window, point size and point type parameters are set to 960x960, 1 and `point', respectively. A horizontal and a vertical circle both with a radius of 5,000 are selected successively as the virtual camera path with the center of circles at the geometry center of an object. The remaining parameters are set as default. These settings preserves detail information as much as possible while maintaining the original point clouds to be watertight. One viewpoint is generated every two degrees on these circles, resulting in 360 image frames for each point cloud. Each distorted clip is then concatenated horizontally with its pristine counterpart into a 10-second video sequence for presentation.

More details about raw MOS processing please check our paper.

-----------COPYRIGHT NOTICE STARTS WITH THIS LINE------------ Copyright (c) 2021 The Qingdao University and University of Waterloo All rights reserved.

Permission is hereby granted, without written agreement and without license or royalty fees, to use, copy, modify, and distribute this database (the polint cloud, the results and the source files) and its documentation for any purpose, provided that the copyright notice in its entirity appear in all copies of this database, and the original source of this database, Intelligent Multimedia Signal Processing (IMSP) Laboratory at Qingdao University and Image & Vision Computing (IVC) Laboratory at University of Waterloo, is acknowledged in any publication that reports research using this database. 
