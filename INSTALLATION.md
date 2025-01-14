# Installation on services.autretechlab.cloud 
(AWS EC2 - Ubuntu 20.04)

## ROS2 Foxy

### Set locale
- `sudo apt update && sudo apt install locales`
- `sudo locale-gen en_US en_US.UTF-8`
- `sudo update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8`
- `export LANG=en_US.UTF-8`

### Setup Sources
- `do apt update && sudo apt install curl gnupg2 lsb-release`
- `curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -`
- `sudo sh -c 'echo "deb [arch=$(dpkg --print-architecture)] http://packages.ros.org/ros2/ubuntu $(lsb_release -cs) main" > /etc/apt/sources.list.d/ros2-- latest.list'`

### Install ROS 2 packages
- `sudo apt update`
- `sudo apt install ros-foxy-ros-base`
- `source /opt/ros/foxy/setup.bash`
- `sudo apt install python3-colcon-common-extensions`

# Python
- `sudo apt install -y python3-pip`
- `pip3 install -U argcomplete`

### Tornado web application server: 
- `pip3 install --user tornado`
- `pip3 install ws4py`

# npm
- `sudo apt install npm` 

# Configure AutreTechLab/ATL_Robotics_IDE
-`git clone https://github.com/AutreTechLab/ATL_Robotics_IDE.git`
- `cd ~/ATL_Robotics_IDE/webapp_root/nodejs`
- `npm install`
- `cd ~/ATL_Robotics_IDE/ros2_ws`
- `source /opt/ros/foxy/setup.bash`
- `colcon build`
- `. ./env.bash`



# TODO Webots and Cozmo no longer needed on this module 
### WeBots
- `wget -qO- https://cyberbotics.com/Cyberbotics.asc | sudo apt-key add -`
- `sudo apt-add-repository 'deb https://cyberbotics.com/debian/ binary-amd64/'`
- `sudo apt-get update`
- `sudo apt-get install webots`

### Cozmo SDK : 
- `pip3 install cozmo`
   - `Successfully installed cozmo-1.4.10 cozmoclad-3.4.0`


