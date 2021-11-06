cmake_minimum_required(VERSION 3.0.2)

project(nato_vise_integration)

## Find catkin macros and libraries
find_package(catkin REQUIRED
  rospy
  nav_msgs
  geometry_msgs
)

catkin_package()

# Install python nodes
install(
  PROGRAMS nodes/vise_converter_node
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)

# Install launch files
install(
  DIRECTORY launch
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)

# Install config files
install(
  DIRECTORY config
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)