=====================
MoveIt! Installation
=====================

2.1. MoveIt! binary installation (recommended):
-------------------------------------------------

::

  sudo apt-get install ros-kinetic-moveit

2.2 MoveIt! Source Installation:
----------------------------------

First, update ros packages and dist packages: ::

  rosdep update
  sudo apt-get update
  sudo apt-get dist-upgrade

Second, install required tools: ::

  sudo apt-get install python-wstool python-catkin-tools clang-format-3.8

Third, create a local workspace and source ROS workspace: ::

  mkdir ~/ws_moveit
  cd ~/ws_moveit
  source /opt/ros/kinetic/setup.bash

Fourth, download and build MoveIt!: ::

  wstool init src
  wstool merge -t src https://raw.githubusercontent.com/ros-planning/moveit/kinetic-devel/moveit.rosinstall
  wstool update -t src
  rosdep install -y --from-paths src --ignore-src --rosdistro kinetic
  catkin config --extend /opt/ros/${ROS_DISTRO} --cmake-args -DCMAKE_BUILD_TYPE=Release
  catkin_make
