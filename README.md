# 3D Mapping and Localization of Mobile Robots using LiDAR Sensor

This repository presents the resources used to carry out the master's thesis presented in the Postgraduate Program in Electrical Engineering at the Federal University of Bahia.

Among the main abilities of autonomous robots, mapping and pose estimation are among the fundamental tasks in mobile robotics. A great effort has been applied by the academic community to achieve, in real time, simultaneous localization and mapping estimation (SLAM) with data from visual sensors or LiDAR sensors.

The objective of the research was to study and implement SLAM techniques using data from LiDAR sensors, to obtain mapping and localization in indoor environments for navigation tasks with mobile robots. In this context,
the LeGO-LOAM, A-LOAM and F-LOAM techniques, aiming to analyze the influence of the volume of geometric static references on the quality of mapping and accuracy of instantaneous location.


## Dependencies
  
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


## Resources

Falar dos algoritmos utilizados

Falar do Optitrack

Falar do Velodyne

Falar dos recursos de simulação

Falar dos mundos criados e motivação


## Results:

Resultados


## Publications: 

An article with the partial results of this dissertation was presented at the 26th International Conference on Climbing and Walking Robots and the Support Technologies for Mobile Machines, held in 2023 in the city of Florianópolis-SC.

### Reference for access:
de Carvalho, M.E.C., Ribeiro, T.T., Conceicao, A.G.S. (2024). Comparative Analysis of LiDAR SLAM Techniques in Simulated Environments in ROS Gazebo. In: Youssef, E.S.E., Tokhi, M.O., Silva, M.F., Rincon, L.M. (eds) Synergetic Cooperation between Robots and Humans. CLAWAR 2023. Lecture Notes in Networks and Systems, vol 811. Springer, Cham.

