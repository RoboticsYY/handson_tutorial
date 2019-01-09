===================
1. Getting Started
===================

1.1 Setup the handson code: 
------------------------------

::

  sudo docker exec -t -i moveit_handson bash
  catkin_make -DCMAKE_BUILD_TYPE=Release
  source devel/setup.bash

You can check the installation by run: ::

  roslaunch handson_description visualize_ur5.launch

If everything works fine, you can see the following screen.

.. image:: ../_static/visualization.png



