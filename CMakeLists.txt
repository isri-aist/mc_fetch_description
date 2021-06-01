cmake_minimum_required(VERSION 3.0.2)
project(mc_fetch_description)

find_package(catkin REQUIRED COMPONENTS
  fetch_description
)

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES mc_fetch_description
#  CATKIN_DEPENDS fetch_description
#  DEPENDS system_lib
)

include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)

