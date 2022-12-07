# ecse373_f22_zxj223_bags_and_playback

# Laboratory#3a

## 1. Dependency
This repo is a ROS package that contain a basic robot model and can view the moving route and the map of glennan 5th floor. 
Dependency:
1. ROS Neotic
2. ROS joint-state-publisher-gui
3. gazebo-plugins
4. ROS velodyne-description
5. ROS map


## 2. Quick command for view the robot model of lab3:

The basic command to view the robot model and the moving route in RVIZ is:

`roslaunch bags_and_playback bags_and_palyback.launch`

## Args of launch the robot model can be modified:

`"bag_path": Point to the bag file path`

Also, in order to successfully show the map in RVIZ, you show put the map server file under `catkin_ws/src`

**The file named "update_navvis_description_for_lab2.launch" is the updated launch file of lab2, also the git repo of lab2 has been updated too**


## 3.The command to view the robot model of lab 2:
1. View the robot model using Joint_state_publisher GUI:

`roslaunch navvis_description navvis_description.launch`

2. View the robot model without Joint_state_publisher GUI:

`roslaunch navvis_description navvis_description.launch use_gui:=false` 

The parameter `use_xacro` can be used to decide that viewing the robot model using URDF file or XACRO file.
ex:

Command for viewing the robot model using XACRO file with joint_state_publisher GUI:

`roslaunch navvis_description navvis_description.launch use_xacro:=true`

parameter use_robot_state_publisher` can be used to decide to start robot_state publisher which takes information about joints and
creates transforms published on the /tf and /tf_static topics or not.

Command for viewing the robot model robot_state_publisher:

`roslaunch navvis_description navvis_description.launch use_robot_state_publisher:=true`
