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

Para a realização deste trabalho foram utilizados três variantes do algoritmo LOAM-Velodyne, que é uma versão adaptada para sensor Velodyne do algoritmo desenvolvido por Zhang e Singh (2017).

A técnica LeGO-LOAM (Lightweight and Ground Optimized LOAM) apresentada por Shan and Englot (2018) é uma versão mais leve do LOAM, otimizada para veículos terrestres que obtém estimativas de pose online, podendo ser utilizada em um sistema embarcado de baixo consumo energético

A-LOAM (Advanced LOAM) é uma implementação avançada da técnica LOAM-Velodyne, com o uso de Eigen e Ceres Solver para simplificar a estrutura do código.

A estratégia F-LOAM (Fast LiDAR Odometry and Mapping), que busca uma solução de menor custo computacional e em tempo real, utilizando um método não iterativo, de dois estágios de compensação de distorção. 

Os trés algoritmos foram testados em ambientes simulados e em ambientes reais, com o objetivo de analisar o desempenho das técnicas para estimação de localização e mapeamento. A Figura 1 abaixo ilustra o modelo do robô móvel Huusky UGV A200, utilizado no Gazebo, com o sensor LiDAR 3D Velodne VLP 16 posicionado sobre a base superior, e a Fugura 2 ilustram a imagem do arranjo real utilizado para aquisição de dados.


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


Para os ambientes simulados os resultados obtidos pelos algoritmos foram comparados com o Ground Truth do robô Husky UGV A200. Para os ambientes reais foi utilizado o sistema de localização Optitrackm que conforme apresentado na Figura 3, é composto por um conjunto de câmeras capazes de detectar a localização dos marcadores esféricos que foram posicionados próximo ao sensor LiDAR 3D Velodyne VLP 16.

<p align='center'>
    Figure 3- Robô Husky equipamento com sensor LiDAR Velodyne VLP 16.
</p>
<p align='center'>
    <img src="/Images/Cameras_Optitrack.jpeg" alt="drawing" width="400"/>
</p>


Para avaliação do desempenho dos algoritmos LiDAR SLAM, em ambientes simulados, foram utilizados quatro ambientes no simulador Gazebo. O objetivo foi avaliar o comportamento dos algoritmos em ambientes com poucas e com diversas features geométricas e a influência do deslocamento em linha reta e na presença de curvas. As Figuras 4, 5 e 6 ilustram os mundos criados no Gazebo.

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





## Results:

Resultados

<p align='center'>
    Figure XX- Robô Husky equipamento com sensor LiDAR Velodyne VLP 16.
</p>
<p align='center'>
    <img src="/Images/Cameras_Optitrack.jpeg" alt="drawing" width="400"/>
</p>



## Publications: 

An article with the partial results of this dissertation was presented at the 26th International Conference on Climbing and Walking Robots and the Support Technologies for Mobile Machines, held in 2023 in the city of Florianópolis-SC.

### Reference for access:
de Carvalho, M.E.C., Ribeiro, T.T., Conceicao, A.G.S. (2024). Comparative Analysis of LiDAR SLAM Techniques in Simulated Environments in ROS Gazebo. In: Youssef, E.S.E., Tokhi, M.O., Silva, M.F., Rincon, L.M. (eds) Synergetic Cooperation between Robots and Humans. CLAWAR 2023. Lecture Notes in Networks and Systems, vol 811. Springer, Cham.

