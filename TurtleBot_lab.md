# Set Network
robot | pc 
---| --- 
ROS_MASTER_URI = http://<pc_ip>:11311 | ROS_MASTER_URI = http://<pc_ip>:11311
ROS_HOSTNAME=<robot_ip> | ROS_MASTER_URI = <pc_ip>
 \ | step 1: roscore
step 2: roslaunch turtlebot3_bringup turtlebot3_robot.launch | \
\ | step 3: roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
\ | step 5 : [run gmapping] roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping  
\ | step 4 optional :roslaunch realsense_camera r200_nodelet_rgbd.launch [run realsence](http://emanual.robotis.com/docs/en/platform/turtlebot3/appendix_realsense/#run-realsense_camera-node)
