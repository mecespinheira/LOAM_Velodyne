# Mapeamento 3D e Localização de Robôs Móveis utilizando Sensor LiDAR

Este repositório apresenta os recursos utilizados para realização da dissertação de mestrado apresentada no Programa de Pós-Graduação em Engenharia Elétrica da Universidade Federal da Bahia.

Entre as principais habilidades dos robôs autônomos, o mapeamento e a estimativa de pose, estão entre as tarefas fundamentais na robótica móvel. Um grande esforço tem sido aplicado pela comunidade acadêmica para alcançar, em tempo real, uma estimativa de localização e mapeamento simultâneos (SLAM) com dados provenientes de sensores visuais ou de sensores LiDAR.

O objetivo da pesquisa foi estudar e implementar técnicas SLAM utilizando dados de sensores LiDAR, para obtenção do mapeamento e localização em ambientes internos (indoor) para tarefas de navegação com robôs móveis. Neste contexto foram implementadas
as técnicas LeGO-LOAM, A-LOAM e F-LOAM, objetivando analisar a influência do volume de referenciais estáticos geométricas na qualidade do mapeamento e precisão da localização instantânea.


## Dependências
  
- [ROS](http://wiki.ros.org/ROS/Installation) (tested with indigo, kinetic, and melodic)
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

