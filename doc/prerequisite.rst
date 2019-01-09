=========================================
Prerequisite (Skip, exist in dock image)
=========================================

The installation and environment configuration in this section are already included 
in the docker image we provided. You can skip this section.

- Ubuntu 16.04
- ROS Kinetic desktop full http://wiki.ros.org/kinetic/Installation/Ubuntu
- MoveIt http://moveit.ros.org/install/

:: 

  sudo apt install ros-kinetic-moveit ros-kinetic-moveit-resources ros-kinetic-moveit-visual-tools ros-kinetic-panda-moveit-config ros-kinetic-geometric-shapes ros-kinetic-tf2-geometry-msgs

Install necessary debian packages: :: 

  sudo apt install python-rosinstall python-rosinstall-generator python-wstool build-essential
  sudo apt install python-wstool python-catkin-tools clang-format-3.8
  sudo apt install ros-kinetic-universal-robot
  sudo apt install ros-kinetic-ur-description

Install handson source code: ::

  echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc
  mkdir -p ~/ws_handson/src
  cd ~/ws_handson/src
  git clone https://github.com/RoboticsYY/moveit_handson.git
  git clone https://github.com/RoboticsYY/moveit_core_handson.git
  git clone https://github.com/RoboticsYY/moveit_ros_handson.git
  cd ..
  catkin_make -DCMAKE_BUILD_TYPE=Release

More information: 

Onsite technical support: OTC Robotics Engineering Team