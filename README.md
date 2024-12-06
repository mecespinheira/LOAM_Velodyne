# 3D Mapping and Localization of Mobile Robots using LiDAR Sensor

This repository presents the resources used to carry out the master's thesis presented in the Postgraduate Program in Electrical Engineering at the Federal University of Bahia, Salvador, Brazil.

Among the main abilities of autonomous robots, mapping and pose estimation are among the fundamental tasks in mobile robotics. A great effort has been applied by the academic community to achieve, in real time, simultaneous localization and mapping estimation (SLAM) with data from visual sensors or LiDAR sensors.

The objective of the research was to study and implement SLAM techniques using data from LiDAR sensors, to obtain mapping and localization in indoor environments for navigation tasks with mobile robots. In this context,
the LeGO-LOAM, A-LOAM and F-LOAM techniques, aiming to analyze the influence of the volume of geometric static references on the quality of mapping and accuracy of instantaneous location.

## Author Information

Authors: Marcelo Espinheira Cravo de Carvalho, André Gustavo Scolari Conceição and Tiago Trindade Ribeiro

M. E. C. de Carvalho, A. G. S. Conceiçãoo and T. T. Ribeiro are from the LaR - Robotics Laboratory, Department of Electrical and Computer Engineering, Federal University of Bahia, Salvador, Brazil. E-mails: mec.espinheira@gmail.com, andre.gustavo@ufba.br, tiagotr@ufba.br. 

## Prerequisites
  
- [ROS](http://wiki.ros.org/ROS/Installation) (tested with noetic)
- [gtsam](https://github.com/borglab/gtsam/releases) (Georgia Tech Smoothing and Mapping library, 4.0.0-alpha2)
  ```
  wget -O ~/Downloads/gtsam.zip https://github.com/borglab/gtsam/archive/4.0.0-alpha2.zip
  cd ~/Downloads/ && unzip gtsam.zip -d ~/Downloads/
  cd ~/Downloads/gtsam-4.0.0-alpha2/
  mkdir build && cd build
  cmake ..
  sudo make install
  ```
- [Ceres Solver](http://ceres-solver.org/installation.html)
- [PCL](http://www.pointclouds.org/downloads/linux.html)
- [Clearpath Husky](https://github.com/husky/husky)
- [LeGO-LOAM](https://github.com/RobustFieldAutonomyLab/LeGO-LOAM)
- [A-LOAM](https://github.com/HKUST-Aerial-Robotics/A-LOAM)
- [F-LOAM](https://github.com/wh200720041/floam)


## Resources

To carry out this work, three variants of the LOAM-Velodyne algorithm were used, which is a version adapted for the Velodyne sensor of the algorithm developed by Zhang and Singh (2017).

The [LeGO-LOAM](https://github.com/RobustFieldAutonomyLab/LeGO-LOAM) (Lightweight and Ground Optimized LOAM) technique presented by Shan and Englot (2018) is a lighter version of LOAM, optimized for ground vehicles that obtains online pose estimates, which can be used in a low-energy embedded system

[A-LOAM](https://github.com/HKUST-Aerial-Robotics/A-LOAM) (Advanced LOAM) is an advanced implementation of the LOAM-Velodyne technique, using Eigen and Ceres Solver to simplify the structure of the code.

The [F-LOAM](https://github.com/wh200720041/floam) (Fast LiDAR Odometry and Mapping) strategy, which seeks a lower computational cost and real-time solution, using a non-iterative, two-stage method distortion compensation. 

The three algorithms were tested in simulated and real environments, with the aim of analyzing the performance of the techniques for location estimation and mapping. Figure 1 below illustrates the Husky UGV A200 mobile robot model, available in the [Clearpath Husky](https://github.com/husky/husky) package , with the Velodne VLP 16 3D LiDAR sensor positioned on the upper base, and Figure 2 illustrates the image of the real array used for data acquisition.


<p align='center'>
    Figure 1- Model of the Husky UGV A200 mobile robot.
</p>
<p align='center'>
    <img src="/Images/Husky_UGV_A200.png" alt="drawing" width="400"/>
</p>

<p align='center'>
    Figure 2- Husky robot equipment with Velodyne VLP 16 LiDAR sensor.
</p>
<p align='center'>
    <img src="/Images/Husky_LAR_1.jpeg" alt="drawing" width="400"/>
</p>

For the simulated environments, the results obtained by the algorithms were compared with the Ground Truth of the Husky UGV A200 robot. For real environments, the Optitrack localization system was used, which, as shown in Figure 3, is composed of a set of cameras capable of detecting the location of spherical markers that were positioned close to the Velodyne VLP 16 3D LiDAR sensor, as can be seen in Figure 2.

<p align='center'>
    Figure 3- Robô Husky equipamento com sensor LiDAR Velodyne VLP 16.
</p>
<p align='center'>
    <img src="/Images/Cameras_Optitrack.jpeg" alt="drawing" width="400"/>
</p>

To evaluate the performance of the LiDAR SLAM algorithms, in simulated environments, four environments were used in the Gazebo simulator. The objective was to evaluate the behavior of the algorithms in environments with few and diverse geometric features and the influence of displacement in a straight line and in the presence of curves. Figures 4, 5 and 6 illustrate the worlds created in Gazebo.

<p align='center'>
    Figure 4- Straight hallway without window.
</p>
<p align='center'>
    <img src="/Images/Hall_without_window.png" alt="drawing" width="400"/>
</p>


<p align='center'>
    Figure 5- Straight hallway with window.
</p>
<p align='center'>
    <img src="/Images/Hall_with_window.png" alt="drawing" width="400"/>
</p>


<p align='center'>
    Figure 6- Closed square corridor without window.
</p>
<p align='center'>
    <img src="/Images/Hall_closed_without_window.png" alt="drawing" width="400"/>
</p>

To analyze the algorithms in simulated environments, an environment developed in Gazebo was also used, which has the same dimensions and the same arrangement of tables and chairs as that found in the Robotics Laboratory (LaR) at the Federal University of Bahia, as shown in Figure 7. The performance analysis in a real environment was carried out in the university's real Robotics Laboratory, which allowed a comparative analysis between the performance of the algorithms for localization and mapping in simulated environments and in real environments.

<p align='center'>
    Figure 7- Simulated environment of the Robotics Laboratory at the Federal University of Bahia.
</p>
<p align='center'>
    <img src="/Images/LaR.jpg" alt="drawing" width="400"/>
</p>

## Results:

Os resultados obtidos com as técnicas foram análisados a partir dos gráficos da trajetória gerada a partir da estimativa de localização instântanea e dos mapas tridimensionais gerados. As Figuras 8, 9 e 10 apresentam os gráficos das trajetórias estimadas pelos algoritmos no Laboratório de Robótica simulado, para os algortimos LeGO-LOAM, A-LOAM e F-LOAM respectivamente.

<p align='center'>
    Figure 8- Point cloud mapping in the LaR environment simulated in Gazebo using the LeGO-LOAM algorithm.
</p>
<p align='center'>
    <img src="/Images/Simulation_LeGO-LOAM.jpg" alt="drawing" width="400"/>
</p>

<p align='center'>
    Figure 9- Point cloud mapping in the LaR environment simulated in Gazebo using the A-LOAM algorithm.
</p>
<p align='center'>
    <img src="/Images/Simulation_A-LOAM.jpg" alt="drawing" width="400"/>
</p>

<p align='center'>
    Figure 10- Point cloud mapping in the LaR environment simulated in Gazebo using the F-LOAM algorithm.
</p>
<p align='center'>
    <img src="/Images/Simulation_F-LOAM.jpg" alt="drawing" width="400"/>
</p>


## Publications: 

An article with the partial results of this dissertation was presented at the 26th International Conference on Climbing and Walking Robots and the Support Technologies for Mobile Machines, held in 2023 in the city of Florianópolis-SC.

### Reference for access:
de Carvalho, M.E.C., Ribeiro, T.T., Conceicao, A.G.S. (2024). Comparative Analysis of LiDAR SLAM Techniques in Simulated Environments in ROS Gazebo. In: Youssef, E.S.E., Tokhi, M.O., Silva, M.F., Rincon, L.M. (eds) Synergetic Cooperation between Robots and Humans. CLAWAR 2023. Lecture Notes in Networks and Systems, vol 811. Springer, Cham.

