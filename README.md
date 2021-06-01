# Additional description files for Fetch robot
This package has additional convex and rsdf files for Fetch to use mc_rtc.
Fetch robot has urdf, collada and meshes in the original `fetch_description` package.

It contains the following directories:
- `convex/`: convex hulls (generated from pointclouds sampled from the dae meshes)
- `rsdf/`: Special urdf-like format describing surfaces attached to links on the robot

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
