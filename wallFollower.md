|robot                                                        | pc                                                                                      |
|-------------------------------------------------------------| ----------------------------------------------------------------------------------------|
|ROS_MASTER_URI = http://<pc_ip>:11311                        | ROS_MASTER_URI = http://<pc_ip>:11311                                                   |
|ROS_HOSTNAME=<robot_ip>                                      | ROS_MASTER_URI = <pc_ip>                                                                |
| \                                                           | step 1: roscore                                                                         |
| \                                                           | step 2: roslaunch turtlebot3_bringup turtlebot3_remote.launch                           |
|step 2: roslaunch turtlebot3_bringup turtlebot3_robot.launch | \                                                                                       |
|\                                                            | step 3: roslaunch comp3431_starter wallFollow.launch                                    |
|\                                                            | step 4: in python, run comp3431_starter/scripts/cmd_controller.py, then type "start"    |
