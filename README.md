# Additional description files for Fetch robot
This package has additional convex and rsdf files for Fetch to use mc_rtc.
Fetch robot has urdf, collada and meshes in the original `fetch_description` package.

It contains the following directories:
- `convex/`: convex hulls (generated from pointclouds sampled from the dae meshes)
- `rsdf/`: Special urdf-like format describing surfaces attached to links on the robot
- `launch/`: launch file and rviz file

## Installation

### ROS environment

On an environment with ROS and catkin properly setup (on ubuntu, you need the `catkin-python-tools` package)

```sh
cd <catkin_data_ws>/src
git clone https://github.com/mc_fetch_description
cd ..
catkin build
```

## Dependencies

- fetch_description
- [mesh_sampling](https://github.com/arntanguy/mesh_sampling)
- qhull-bin

## Generation of convex files
To run the conversion, simply run

```sh
cd scripts
./generate_convex.sh
```
If your catkin environment is sourced `source ~/catkin_ws/install/setup.bash`, the robot model will be available to all ROS tools, and mc_rtc robot module.

To display the robot, you can use:

```
$ roslaunch mc_fetch_description display_fetch.launch
```

 - If you have mc_rtc and the corresponding robot module installed, you can use the `convexes:=True` or `surfaces:=True` arguments to display the robot convexes and surfaces.

