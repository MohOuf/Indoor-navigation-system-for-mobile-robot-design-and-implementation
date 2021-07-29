# Indoor navigation system for mobile robot design and implementation

**Using ubuntu 16.04 and ROS kinetic **


### 1.01: Installing ROS kinetic using : 
 $ sudo apt-get update
 $ sudo apt-get upgrade
 $ wget https://raw.githubusercontent.com/ROBOTIS-GIT/robotis_tools/master/install_ros_kinetic.sh
 $ chmod 755 ./install_ros_kinetic.sh 
 $ bash ./install_ros_kinetic.sh
### 1.02: installing ROS Kinetic packages using : 
$ sudo apt-get install ros-kinetic-joy ros-kinetic-teleop-twist-joy \
 ros-kinetic-teleop-twist-keyboard ros-kinetic-laser-proc \
 ros-kinetic-rgbd-launch ros-kinetic-depthimage-to-laserscan \
 ros-kinetic-rosserial-arduino ros-kinetic-rosserial-python \
 ros-kinetic-rosserial-server ros-kinetic-rosserial-client \
 ros-kinetic-rosserial-msgs ros-kinetic-amcl ros-kinetic-map-server \
 ros-kinetic-move-base ros-kinetic-urdf ros-kinetic-xacro \
 ros-kinetic-compressed-image-transport ros-kinetic-rqt* \
 ros-kinetic-gmapping ros-kinetic-navigation ros-kinetic-interactive-markers
### 2.01: installing TurtleBot3 Packages using : 
  $ sudo apt-get install ros-kinetic-dynamixel-sdk
  $ sudo apt-get install ros-kinetic-turtlebot3-msgs 
  $ sudo apt-get install ros-kinetic-turtlebot3
## 3: Using steps below to install the simulation  packages

### 3.01: install the simulation using : 
 $ cd ~/catkin_ws/src/
 $ git clone -b melodic-devel https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
 $ cd ~/catkin_ws && catkin_make
### 3.02: (open new Terminal) Then write the path below : 
 $ source ~/catkin_ws/devel/setup.bash
### 3.03: To lunch the simulation : 
 $ export TURTLEBOT3_MODEL=burger
 $ roslaunch turtlebot3_gazebo turtlebot3_world.launch

## 4:Lunching (Slam Node, Teleoperation Node)
### 4.01: Lunch the Slam node: 
 $ export TURTLEBOT3_MODEL=burger
 $ roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping
### 4.02: Lunch the Teleoperation node: 
 $ export TURTLEBOT3_MODEL=burger
 $ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch

### 5: To save the map after modifying: 
$ rosrun map_server map_saver -f ~/map


## Some Images for the Map : 
![124581707-00656500-de5a-11eb-9eff-6709d2dca799](https://user-images.githubusercontent.com/83540265/125212052-7121dc80-e2b3-11eb-86b2-60b32d92a923.png)

![124582239-8386bb00-de5a-11eb-80a7-7608c8cdc82b](https://user-images.githubusercontent.com/83540265/125212046-649d8400-e2b3-11eb-9f50-48458b1d9a7e.png)

