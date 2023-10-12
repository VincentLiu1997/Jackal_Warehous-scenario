# Instruction

## 1. Create your workspace and build the environment
```
$ mkdir -p ~/Jackal_ws/src
$ cd ~/Jack_ws/src && git clone https://github.com/VincentLiu1997/Jackal_Warehous-scenario.git
$ cd ~/Jack_ws/ && catkin_make
```
## 2. Run Gazebo simulation 
```
$ roslaunch jackal_gazebo jackal_world.launch config:=front_laser
```
## 3. Launch the AMCL demo and run the navigation
Open a new terminal.
```
$ roslaunch jackal_navigation amcl_demo.launch map_file:=/YOURPATH/mymap1.yaml
```
Open a new terminal.
```
$ roslaunch jackal_viz view_robot.launch config:=localization
```
You can use Set NAV goal for navigation NOW!
## 4. Point Operation and Patrol
```
$ rosrun send_goals point_navigation.py
```
OR
```
$ rosrun send_goals patrol.py
```
