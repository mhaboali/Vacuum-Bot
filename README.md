# Vacuum-Bot
The Vacuum-Bot is a vacuum cleaner robot, where we installed many ROS packages to make it Autonomous robot based on Gazebo simulations and real-time deployment

![Screenshot from 2019-04-20 14-57-57](https://user-images.githubusercontent.com/29764281/56891962-7140b380-6a7e-11e9-8c61-ed58786cda7d.png)

![Screenshot from 2019-04-29 13-11-27](https://user-images.githubusercontent.com/29764281/56892742-dc8b8500-6a80-11e9-9e2b-da6d5338c5b0.png)

## Dependencies
1. Ubuntu 16.04
2. ROS Kinetic
3. Gazebo-7
4. ROS-Nav Stack
5. tf packages

## Setup the repo on your local machine
1. Clone the repo under $HOME
2. cd inside the repo directory then cd into catkin_ws/
3. run " catkin clean "
4. run " catkin build "
5. run " source devel/setup.bash "

## Running the Simulation
#### Gazebo Environment
  run " roslaunch vaccum_robot vaccum_robot.launch "
#### SLAM & Move-base Nodes
  run " roslaunch vaccum_bot_navigation gmapping_demo.launch "
#### Launching the Rviz
  run " rosrun rviz rviz " then load this file " src/vaccum_robot/vaccumbot_viz.rviz "
#### Send goals to the robot
  run " rostopic pub /move_base_simple/goal geometry_msgs/PoseStamped '{header: {stamp: now, frame_id: "/map"}, pose: {position: {x: 0.0, y: 0.0, z: 0.0}, orientation: {w: 1.0}}} "
