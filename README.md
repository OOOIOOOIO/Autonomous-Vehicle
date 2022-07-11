# Autonomous-Vehicle
How to install Cuda10-2 and ROS(melodic) in Ubuntu18.04

<hr>

# Cuda10-2

link : https://developer.nvidia.com/cuda-10.2-download-archive?target_os=Linux&target_arch=x86_64&target_distro=Ubuntu&target_version=1804&target_type=deblocal

### choose
- Operating System : Linux
- Architectrue : x86_64
- Distribution : Ubuntu
- Installer Type : deb(local)


### At terminal
```
wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/cuda-ubuntu1804.pin

sudo mv cuda-ubuntu1804.pin /etc/apt/preferences.d/cuda-repository-pin-600

wget https://developer.download.nvidia.com/compute/cuda/10.2/Prod/local_installers/cuda-repo-ubuntu1804-10-2-local-10.2.89-440.33.01_1.0-1_amd64.deb

sudo dpkg -i cuda-repo-ubuntu1804-10-2-local-10.2.89-440.33.01_1.0-1_amd64.deb

sudo apt-key add /var/cuda-repo-10-2-local-10.2.89-440.33.01/7fa2af80.pub

sudo apt-get update

sudo apt-get -y install cuda10-2

```

### How to check version
```
nvcc -V

or

nvidia-smi
```


<br>
<hr>
<br>

# Ubuntu 18.04(Bionic), Melodic ROS

## At terminal
```
wget https://raw.githubusercontent.com/orocapangyo/meetup/master/190830/install_ros_melodic.sh && chmod 755 ./install_ros_melodic.sh && bash ./install_ros_melodic.sh

source ~/catkin_ws/devel/setup.bash

gedit ~/.bashrc

```
```
export ROS_MASTER_URI=http://localhost:11311
export ROS_HOSTNAME=localhost

--> change

export ROS_MASTER_URI=http://YOUR IP ADDR:11311
export ROS_HOSTNAME=YOUR IP ADDR

```
