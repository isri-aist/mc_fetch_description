# Fetch robot description for [mc_rtc](https://jrl-umi3218.github.io/mc_rtc/)
This package contains additional files to the original [mc_fetch_description](https://github.com/isri-aist/mc_fetch_description) package.

It contains the following directories:
 - `launch/`: launch file and rviz file
 - `updateCMakeLists.txt`: Changed so that related files can be installed in CATKIN_PACKAGE_SHARE_DESTINATION

## Installation

### ROS environment
On an environment with ROS and catkin properly setup:

```
$ cd ~/catkin_ws/src
$ git clone https://github.com/@MC_FETCH_DESCRIPTION_REPOSITORY@  # This repository
$ git clone https://github.com/isri-aist/mc_fetch_description
$ cd mc_fetch_description
$ cp @MC_FETCH_DESCRIPTION_PATH@/updateCMakeLists.txt CMakeLists.txt
$ cp -r @MC_FETCH_DESCRIPTION_PATH@/launch . 
$ cd ~/catkin_ws
$ catkin_make
$ cd build
$ make install
```

If your catkin environment is sourced `source ~/catkin_ws/install/setup.bash`, the robot model will be available to all ROS tools, and mc_rtc robot module.

To display the robot, you can use:

```
$ roslaunch mc_fetch_description display_fetch.launch
```

 - If you have mc_rtc and the corresponding robot module installed, you can use the `convexes:=True` or `surfaces:=True` arguments to display the robot convexes and surfaces.
