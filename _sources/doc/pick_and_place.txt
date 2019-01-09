==================
4. Pick and Place
==================

Bring up MoveIt! motion planning pipeline in one shell. 
Remember to source the workspace before executing the command: ::

  sudo docker exec -t -i moveit_handson bash
  source devel/setup.bash
  roslaunch handson_moveit_config demo.launch

.. note:: this command is executed from the config package just created, 
          if you meet error in this section, you can replace the above command 
          by the following command to see the result: ::

            roslaunch ur5_hitbot_ilc_platform_moveit_config demo.launch

Run the pick and place demo, in which the UR5 robot will pick a ball 
with hitbot gripper from the platform surface and place it at another location: ::

  sudo docker exec -t -i moveit_handson bash
  source devel/setup.bash
  roslaunch handson_example pick_place.launch

.. image:: ../_static/demo_2.gif