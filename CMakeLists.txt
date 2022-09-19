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

# install convex launch rsdf
install(DIRECTORY "${PROJECT_SOURCE_DIR}/convex/" DESTINATION "${CATKIN_PACKAGE_SHARE_DESTINATION}/convex")
install(DIRECTORY "${PROJECT_SOURCE_DIR}/launch/" DESTINATION "${CATKIN_PACKAGE_SHARE_DESTINATION}/launch")
install(DIRECTORY "${PROJECT_SOURCE_DIR}/rsdf/" DESTINATION "${CATKIN_PACKAGE_SHARE_DESTINATION}/rsdf")
