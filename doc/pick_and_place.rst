===============
Pick and Place
===============

Bring up MoveIt! motion planning pipeline in one shell: ::

  roslaunch ur5_hitbot_ilc_platform_moveit_config demo.launch

Run the pick and place demo, in which the UR5 robot will pick a ball 
with hitbot gripper from the platform surface and place it at another location: ::

  roslaunch handson_example pick_place.launch
