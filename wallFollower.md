# WallFollower

### Set-Up:
Git clone http://robolab.cse.unsw.edu.au:4443/comp3431-rsa/comp3431-rsa.git into the catkin_ws/src
1. If you already have already run the VM setup script you can just do a git pull
2. If you have not, then you will need to do an additional git checkout 18s2 command
    
Additionally, clone crosbot here after step 2 if you have not run the setup script.
git clone -b rsa-18s2 --single-branch http://robolab.cse.unsw.edu.au:4443/rescue/crosbot.git 
You will also need to install libnewmat sudo apt-get --assume-yes install libnewmat10-dev
EDIT: Just run the script
https://github.com/awondo/rsa-18s2/blob/master/vm_... 

catkin_make 

### Run wallFollower
|robot                                                        | pc                                                                                      |
|-------------------------------------------------------------| ----------------------------------------------------------------------------------------|
|ROS_MASTER_URI = http://<pc_ip>:11311                        | ROS_MASTER_URI = http://<pc_ip>:11311                                                   |
|ROS_HOSTNAME=<robot_ip>                                      | ROS_MASTER_URI = <pc_ip>                                                                |
| \                                                           | step 1: roscore                                                                         |
| \                                                           | step 2: roslaunch turtlebot3_bringup turtlebot3_remote.launch                           |
|step 2: roslaunch turtlebot3_bringup turtlebot3_robot.launch | \                                                                                       |
|\                                                            | step 3: roslaunch comp3431_starter wallFollow.launch                                    |
|\                                                            | step 4: in python, run comp3431_starter/scripts/cmd_controller.py, then type "start"    |
