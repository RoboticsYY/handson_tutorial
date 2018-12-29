=========================
ROS Kinetic Installation
=========================

If you have already completed all the installation steps in this section, you can directly jump to the next section.

1.1 Setup your computer to accept software from packages.ros.org: 
------------------------------------------------------------------

:: 

  sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'

1.2 Set up your keys:
----------------------

::

  sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 421C365BD9FF1F717815A3895523BAEEB01FA116

1.3 Installation:
-------------------

First, make sure your Debian package index is up-to-date: ::

  sudo apt-get update

Second, install ROS Kinetic Desktop-Full: ::

  sudo apt-get install ros-kinetic-desktop-full

1.4 Initial rosdep:
--------------------

::

  sudo rosdep init
  rosdep update

1.5 Environment setup:
-----------------------

::

  echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc
  source ~/.bashrc
  source /opt/ros/kinetic/setup.bash

1.6 Dependencies for building packages:
----------------------------------------
::

  sudo apt install python-rosinstall python-rosinstall-generator python-wstool build-essential

