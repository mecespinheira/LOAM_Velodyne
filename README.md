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


## Recursos Utilizados

Falar dos algoritmos utilizados

Falar do Optitrack

Falar do Velodyne

Falar dos recursos de simulação

Falar dos mundos criados e motivação


## Como rodar os arquivos

Explicar o passo a passo para realizar as simulações 


## Resultados

Resultados


## Publicações Realizadas 

Falar da publicação no Clawar

