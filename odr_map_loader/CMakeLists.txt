cmake_minimum_required(VERSION 3.0.2)
project(odr_map_loader)

# add_compile_options(-std=c++11)
add_compile_options(-std=c++14 -O3)

find_package(catkin REQUIRED COMPONENTS
  rospy
  roscpp
  std_msgs
  odr_map_msgs
  visualization_msgs
  jsk_recognition_msgs
  odr_map_msgs
  odr_map
)

find_package(XMLRPC REQUIRED)

catkin_package()

include_directories(
  ${catkin_INCLUDE_DIRS}
)

# odr_map_loader
add_executable(odr_map_loader
  src/odr_map_loader.cpp
)

target_link_libraries(odr_map_loader
  ${catkin_LIBRARIES}
)
