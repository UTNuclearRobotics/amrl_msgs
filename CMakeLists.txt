cmake_minimum_required(VERSION 3.0.2)
project(amrl_msgs)

find_package(catkin REQUIRED
  roscpp
  geometry_msgs
  message_generation
)

## Generate messages in the 'msg' folder
add_message_files(DIRECTORY msg)

## Generate services in the 'srv' folder
add_service_files(DIRECTORY srv)

## Generate added messages and services with any dependencies listed here
generate_messages(
  DEPENDENCIES
  std_msgs
  geometry_msgs
)

catkin_package(
  CATKIN_DEPENDS geometry_msgs message_runtime
)