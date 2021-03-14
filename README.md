# ESEKF-IMU-GNSS-Lidar
Sensor fusion between IMU, GNSS and Lidar data using an Error State Extended Kalman Filter.

This ES-EKF implementation breaks down to 3 test cases (for each we present the results down below):
* Phase1: The filter relies on IMU data to propagate the state forward in time, and GPS and LIDAR position updates to correct the state estimate. For this task we use the "pt1_data.pkl" file.
* Phase2: Check the effects of sensor miscalibration (created by an incorrect transformation between the LIDAR and the IMU sensor frame) on the vehicle pose estimates. Here we determine how to adjust the filter parameters (noise variances) to attempt to compensate for these errors. For this task we use the "pt1_data.pkl" file.
* Phase3: Here we explore the effects of sensor dropout, that is, when all external positioning information (from GPS and LIDAR) is lost for a short period of time. For this task we use the "pt3_data.pkl" file.

### System Results
## Phase 1
![alt text](https://github.com/NekSfyris/ESEKF-IMU-GNSS-Lidar/blob/master/result_images/phase1_1.png)
![alt text](https://github.com/NekSfyris/ESEKF-IMU-GNSS-Lidar/blob/master/result_images/phase1_2.png)

## Phase 2
![alt text](https://github.com/NekSfyris/ESEKF-IMU-GNSS-Lidar/blob/master/result_images/phase2_1.png)
![alt text](https://github.com/NekSfyris/ESEKF-IMU-GNSS-Lidar/blob/master/result_images/phase2_2.png)

## Phase 3
![alt text](https://github.com/NekSfyris/ESEKF-IMU-GNSS-Lidar/blob/master/result_images/phase3_1.png)
![alt text](https://github.com/NekSfyris/ESEKF-IMU-GNSS-Lidar/blob/master/result_images/phase3_2.png)
