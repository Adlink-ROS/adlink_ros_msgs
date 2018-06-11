cmake_minimum_required(VERSION 2.8.3)
project(adlink_msgs)

## Compile as C++11, supported in ROS Kinetic and newer
# add_compile_options(-std=c++11)

## Find catkin macros and libraries
find_package(catkin REQUIRED COMPONENTS
  roscpp
  std_msgs
  geometry_msgs
  message_generation
)


## custom message
add_message_files(
  FILES
  Person.msg
  PersonArray.msg
)

generate_messages(
  DEPENDENCIES
  std_msgs
  geometry_msgs
)


catkin_package(
    CATKIN_DEPENDS std_msgs geometry_msgs message_runtime
)


