# The WPC Database
This database made by Honglei Su (suhonglei@qdu.edu.cn) from University of Waterloo, we welcome everyone to carry on the test and propose the modification opinion. If you use our database https://drive.google.com/drive/folders/1dHDqKXgvkUhQdUzT7pJjrJ7zRnceFIkO?usp=sharing in your paper, please cite our paper: 

[1] Qi Liu, Honglei Su, Zhengfang Duanmu et al. Perceptual Quality Assessment of Colored 3D Point Clouds, submitted to IEEE Trans. Broadcasting.

[2] Honglei Su, Zhengfang Duanmu, Wentao Liu et al., Perceptual Quality Assessment of Colored 3D Point Clouds, 2019 IEEE International Conference on Image Processing (ICIP), IEEE, 2019.

Motivated by the lack of source 3D point cloud, we gather acollection of objects with diverse geometric and textural complexity,  including  snacks,  fruits,  vegetables,  office  supplies,and containers, etc. The selected contents are moderate in sizeand are omni-directionally acquirable. The figures show snapshots of the objects and their characteristics in the WPC database.

![image](https://github.com/qdushl/Waterloo-Point-Cloud-Database/blob/main/Snapshots.jpg)
![image](https://github.com/qdushl/Waterloo-Point-Cloud-Database/blob/main/Characteristics.jpg)

We choose passive watching instead of interactive watching for subjective tests because the latter creates large variations and inconsistencies in terms of the viewpoints and viewing time between subjects and viewing sessions. We employ Technicolor renderer to render each point cloud to a video sequence. The rendering window, point size and point type parameters are set to 960x960, 1 and `point', respectively. A horizontal and a vertical circle both with a radius of 5,000 are selected successively as the virtual camera path with the center of circles at the geometry center of an object. The remaining parameters are set as default. These settings preserves detail information as much as possible while maintaining the original point clouds to be watertight. One viewpoint is generated every two degrees on these circles, resulting in 360 image frames for each point cloud. Each distorted clip is then concatenated horizontally with its pristine counterpart into a 10-second video sequence for presentation.

-----------COPYRIGHT NOTICE STARTS WITH THIS LINE------------ Copyright (c) 2021 The Qingdao University and University of Waterloo All rights reserved.

Permission is hereby granted, without written agreement and without license or royalty fees, to use, copy, modify, and distribute this database (the polint cloud, the results and the source files) and its documentation for any purpose, provided that the copyright notice in its entirity appear in all copies of this database, and the original source of this database, Intelligent Multimedia Signal Processing (IMSP) Laboratory at Qingdao University and Image & Vision Computing (IVC) Laboratory at University of Waterloo, is acknowledged in any publication that reports research using this database. 
