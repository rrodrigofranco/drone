# Drone JJRC H68
O JJRC H68 é um drone barato que contém uma câmera 720p embutida. O código no repositório permite controlar totalmente o movimento do drone usando um joystick e receber a imagem da câmera (que pode ser usado para processamento de imagens). O código foi escrito em python 3 e testado em Kali Linux 20.02.
Para analisar o tráfico dos sinais, conectei meu celular no app do drone e fiz uma interceptação man-in-the-middle usando o airodump-ng junto com o Wireshark e descobri que o aplicativo usa o protocolo UDP para enviar os comandos de controle ao drone e o protocolo TCP para enviar vídeos.
https://sites.google.com/site/negocindosica/jjrc%20h68.jpg

# Instalação Packages:
sudo apt-get update
1) gstreamer -
sudo apt-get install gstreamer1.0-tools
sudo apt-get install -y gstreamer1.0-plugins-bad
2) pygame -
sudo apt-get install python3-pygame
3) GUI -
sudo apt-get install -y qt5-default libvtk6-dev
4) tkinter e outros compontentes - 
sudo apt-get install -y python-dev  python-tk  pylint  python-numpy  python3-dev python3-tk pylint3 python3-numpy flake8
5) opencv -
sudo apt-get install libopencv-dev python3-opencv
# Como executar:
1) Conecte no wifi do drone
2) Execute o arquivo: execute_me.py
# O que tem nesse repositório?
Os códigos estão organizados nas seguintes pastas:
1) camera - Todos os codigos relacionados a camera
2) control - Todos os codigos relacionados ao controle do drone
3) general - Codigos gerais
4) sniffes - sniffes da comunicao entre o drone e o aplicativo 
# Terminais Úteis
1) Interceptar a rede wlan0 - tcpdump -vv -nn -i wlan0
2) Verificar processos que podem conflitar no monitoramento - airmon-ng check 
3) Desabilitar processos que podem confiltar no monitoramento - airmon-ng check kill
4) Monitorar a rede - airmon-ng start wlan0
5) Interceptar a rede no modo monitoramento - tcpdump -vv -nn -i wlan0mon
6) Setar o monitoriamento para um canal específico - iwconfig wlan0mon channel 2
7) Comando para visualisar as redes que estão sendo monitoradas pelo adaptador - airodump-ng wlan0mon
8) Monitorar um canal específico - airodump-ng -c 2 wlan0mon
9) Sair do modo monitor - airmon-ng stop wlan0mon
10) Reiniciar configurações de rede - service network-manager restart

