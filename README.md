# PADLoC: LiDAR-Based Deep Loop Closure Detection and Registration Using Panoptic Attention
## Loop CLosure Detection:
It is basically **_improving the mistakes done before_**

Imagine a robot is exploring a mall, trying to make a map of the different stores and hallways. As it moves around, it takes pictures and notes where it sees things like doors, windows, and displays.
However, as the robot keeps moving, small mistakes in its steps and senses can add up, causing its map to get a bit messed up compared to the real layout of the mall.
Loop closure detection helps fix this problem by letting the robot recognize when it has returned to a place it has already been before.


[Loop_closure_detection.webm](https://github.com/vishapraj/PADLoC-LiDAR-Based-Deep-Loop-Closure-Detection-and-Registration-Using-Panoptic-Attention/assets/126682925/da349a42-2c4d-48cc-9190-26847f21105e)

## Handcrafted Methods

### Local Feature-Based Methods-
* Local Features- These methods focus on small, detailed parts of the environment. They look for unique patterns or shapes in the 3D data from the LiDAR sensor.
Imagine the robot sees a distinctive corner of a table or a particular pattern on the floor. It creates a "descriptor" (a kind of digital fingerprint) for these small details.
* Descriptors Used-Tools like Fast Point Feature Histograms (FPFH) and Normal-Aligned Radial Features (NARF) help the robot describe these small parts.

* HOPN Method-This method uses a top-down view and information about the surface normals (directions of surfaces) to make the robot more robust to noise and different viewpoints.

### Global Feature-Based Methods-
These methods create a single, overall fingerprint of the entire scene the robot sees.
Instead of focusing on small parts, the robot summarizes the entire room into one compact descriptor.
* M2DP Method-This method projects the 3D point cloud into multiple 2D planes, calculates density information on these planes, and combines it into a global descriptor.
* Scan Context-This method uses a polar coordinate system to generate an image-like representation of the scene, helping the robot recognize places globally. Extensions add more details like intensity or semantic data (e.g., labels like "door" or "chair").

### Deep Learning-Based Methods-
* PointNetVLAD-This is a deep learning approach built on top of the PointNet architecture. It learns to create compact descriptors automatically from the 3D point cloud data, making it more flexible and potentially more accurate.
