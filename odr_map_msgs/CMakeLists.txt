cmake_minimum_required(VERSION 3.0.2)
project(odr_map_msgs)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  geometry_msgs
  std_msgs
  message_generation
  sensor_msgs
  uuid_msgs
  nav_msgs
)

add_message_files(
  DIRECTORY msg
  FILES
  BoundaryPolygons.msg
  MapBasepath.msg
  MapBoundary.msg
  MapCrosswalk.msg
  MapLane.msg
  MapTrafficLight.msg
  MapTrafficSign.msg
  MapRoadGuard.msg
  MapObject.msg
  MapBasepathID.msg
  MapStopLine.msg
  LaneInformation.msg
  CrossingPoint.msg
)

## Generate added messages and services with any dependencies listed here
generate_messages(
  DEPENDENCIES
  geometry_msgs
  std_msgs
  sensor_msgs
  uuid_msgs
  nav_msgs
)

catkin_package(
  CATKIN_DEPENDS message_runtime roscpp geometry_msgs std_msgs uuid_msgs nav_msgs
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)
