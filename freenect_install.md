# Tutorial Basico Freenect
![Badge em Desenvolvimento](http://img.shields.io/static/v1?label=STATUS&message=EM%20DESENVOLVIMENTO&color=GREEN&style=for-the-badge)

## Instalação dos pacotes dependentes:
```
$ sudo apt-get install git-core cmake freeglut3-dev pkg-config build-essential libxmu-dev libxi-dev libusb-1.0-0-dev
```

## Instalação do repositorio:
```
$ git clone git://github.com/OpenKinect/libfreenect.git

```

Compilando:

```
$ cd libfreenect
$ mkdir build
$ cd build
$ cmake -L ..
$ make
$ sudo make install
$ sudo ldconfig /usr/local/lib64/
```

## Instalação dos pacotes no Workspace :
```
$ cd ~/catkin_ws/src
$ git clone https://github.com/ros-drivers/freenect_stack.git
```

Checar as dependências com rosdep:
```
$ rosdep update
$ rosdep check --from-paths . --ignore-src --rosdistro noetic
$ rosdep install --from-paths . --ignore-src --rosdistro noetic -y
```

Compilando a workspace:
```
$ cd ~/catkin_ws/
$ catkin_make
```

Source:
```
$ source devel/setup.bash
```

Podemos como exemplo rodar um launch para obter a nuvem de pontos:

```
$ roslaunch freenect_launch freenect.launch depth_registration:=true

```

Para a visualização dos topicos do Kinect usamos o rviz, em outro terminal:

```
$ source devel/setup.bash
$ rviz

```


## Configuração Rviz

Primeiro devemos setar o rziv:
