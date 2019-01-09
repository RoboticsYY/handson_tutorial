======================
0. Launch Docker Image
======================

Please follow the command below to install and update docker: ::

  sudo apt update && sudo apt install -y wget
  mkdir -p ~/code/ && cd ~/code

  wget https://raw.githubusercontent.com/RoboticsYY/moveit_handson/master/docker/install_docker.sh
  wget https://raw.githubusercontent.com/RoboticsYY/moveit_handson/master/docker/setup_docker_display.sh

  chmod +x install_docker.sh
  ./install_docker.sh

If you have a laptop we provided, you can skip this step. 
If you have a USB stick we provided, the stick contains the handson docker image ``moveit_handson_demo.tar.tgz``. 
Copy the image to the local disk at first, then please follow the description below 
to decompress and load the image: ::

  sudo apt update && sudo apt install -y tar
  tar -zxvf moveit_handson_demo.tar.tgz
  sudo docker load < moveit_handson_demo.tar

Please refer below command to verify the docker image created successfully on the disk. Run in shell: ::

  sudo docker images

It should show the following information: ::

  REPOSITORY      TAG                  IMAGE ID            CREATED             SIZE
  intel/kinetic   moveit_handson_demo  6643cc4db2e5        5 hours ago         3.47GB

Run following commands to set the operating environment first 
so that x window can pop up within the docker container: ::

  cd ~/code
  chmod +x setup_docker_display.sh
  ./setup_docker_display.sh
  sudo docker run -t -i --rm -v /tmp/.X11-unix:/tmp/.X11-unix:rw -v /tmp/.docker.xauth:/tmp/.docker.xauth:rw -e XAUTHORITY=/tmp/.docker.xauth -e DISPLAY --name moveit_handson intel/kinetic:moveit_handson_demo bash

Run the following command to open multiple container terminals: ::

  sudo docker exec -t -i moveit_handson bash

.. note:: If you want more information on how to use docker, 
          please see the article here for more information: https://docs.docker.com/install/ 

.. note:: If you don’t have a USB stick, you can install the 
          docker image with the following command: ::
            
            sudo docker pull congliu0913/moveit_handson_demo