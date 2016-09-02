cmake_minimum_required(VERSION 2.8.3)
project(robot_teleop)

## Find catkin macros and libraries
find_package(catkin REQUIRED COMPONENTS roscpp geometry_msgs)

include_directories(${catkin_INCLUDE_DIRS})

catkin_package(
  INCLUDE_DIRS
  CATKIN_DEPENDS roscpp geometry_msgs
  DEPENDS
)

###########
## Build ##
###########

add_executable(robot_teleop_joy
    src/robot_joy.cpp)
target_link_libraries(robot_teleop_joy ${catkin_LIBRARIES})

