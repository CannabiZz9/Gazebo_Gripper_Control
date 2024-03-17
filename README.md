# Gazebo_Gripper_Control
This repository is about how to control gripper in ros2 gazebo using keyboard in teleop twist

1. Sudo apt install ros-foxy-gazebo-*
2.	Description
	    Add Transmission
	    Add Plugin gripper_robot_gazebo_system
	    Add plugin name="gazebo_ros2_control_robot" filename="libgazebo_ros2_control.so"
3.  config
	    controllers.yaml
4.  launch
	    edit launch_sim.launch.py
5.  telop twist keyboard
	    edit controller.py

cd Path/articubot_one
colcon build --symlink-install

source install/setup.bash

chmod +x path/to/your/script.py

    chmod +x /home/tien/colcon_ws/articubot_one/install/articubot_one/lib/articubot_one/controller.py
   OR
    chmod +x /home/tien/colcon_ws/articubot_one/controller.py

to test 
ros2 control list_hardware_interfaces
    Status Should Be :
command interfaces
	firstJoint/velocity [claimed]
	....../velocity [claimed]
	lastJoint/velocity [claimed]
state interfaces
	firstJoint/position
	firstJoint/velocity
	...../position
	...../velocity
	lastJoint/position
	lastJoint/velocity

