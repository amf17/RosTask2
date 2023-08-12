# 2nd task of Robotics and AI Department

### Install ROS packages necessary for controlling the TurtleBot.

```
sudo apt install ros-noetic-joy ros-noetic-teleop-twist-joy \
  ros-noetic-teleop-twist-keyboard ros-noetic-laser-proc \
  ros-noetic-rgbd-launch ros-noetic-depthimage-to-laserscan \
  ros-noetic-rosserial-arduino ros-noetic-rosserial-python \
  ros-noetic-rosserial-server ros-noetic-rosserial-client \
  ros-noetic-rosserial-msgs ros-noetic-amcl ros-noetic-map-server \
  ros-noetic-move-base ros-noetic-urdf ros-noetic-xacro \
  ros-noetic-compressed-image-transport ros-noetic-rqt* \
  ros-noetic-gmapping ros-noetic-navigation ros-noetic-interactive-markers \
  ros-noetic-gazebo-ros-pkgs
```

### Install packages for the TurtleBot's servo

```
sudo apt install ros-noetic-dynamixel-sdk
sudo apt install ros-noetic-turtlebot3-msgs
```

### Install TurtleBot3

```
sudo apt install ros-noetic-turtlebot3
```

Then execute the following commands:

```
cd ~/catkin_ws/src/
git clone -b melodic-devel https://github.com/ROBOTIS-GIT/DynamixelSDK.git
git clone -b melodic-devel https://github.com/ROBOTIS-GIT/turtlebot3_msgs.git
git clone -b melodic-devel https://github.com/ROBOTIS-GIT/turtlebot3.git
cd ~/catkin_ws && catkin_make
```
```
echo "source ~/catkin_ws/devel/setup.bash" >> ~/.bashrc
echo "export TURTLEBOT3_MODEL=burger" >> ~/.bashrc
source ~/.bashrc
```

## Starting 

Run SLAM node:
```
roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping
```
```
roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
```

![image](https://github.com/amf17/RosTask2/assets/139582388/b6eae6fe-7c6e-419b-bdb1-ffe1a99978ea)


![image](https://github.com/amf17/RosTask2/assets/139582388/a1b2cb8c-52a4-46f4-96ef-9a28f12a35d2)
