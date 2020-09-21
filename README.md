# drones
O JJRC H66 é um drone barato que contem uma câmera 720p embutida. O código no repositório permite controlar totalmente o movimento do drone usando um joystick e receber a imagem da câmera do drone (que pode ser usado para processamento de imagens). O código foi escrito em python 3 e testado em Kali Linux 20.02.
![alt text](https://sites.google.com/site/negocindosica/jjrc%20h68.jpg)

# Instalação Packages:
sudo apt-get update
1) gstreamer
sudo apt-get install gstreamer1.0-tools
sudo apt-get install -y gstreamer1.0-plugins-bad
2) pygame (Para o uso do Joystick)
sudo apt-get install python3-pygame
3) GUI
sudo apt-get install -y qt5-default libvtk6-dev
4) tkinter e alguns outros compontentes
sudo apt-get install -y python-dev  python-tk  pylint  python-numpy  python3-dev python3-tk pylint3 python3-numpy flake8
5) opencv
sudo apt-get install libopencv-dev python3-opencv
# Como executar:
1) Conecte no wifi do drone
2) Execute o arquivo: execute_me.py
# O que tem nesse repositorio:
Os codigos estao organizados nas seguintes pastas:
1) camera - Todos os codigos relacionados a camera
2) control - Todos os codigos relacionados ao controle do drone
3) general - Codigos gerais
4) sniffes - sniffes da comunicao entre o drone e o aplicativo 
