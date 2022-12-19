cmake_minimum_required(VERSION 3.0.2)
project(casper_auto_msgs)

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
  CenterLanes.msg
  DecisionTrajectory.msg
  Gap.msg
  IntentionTrajectory.msg
  PedestrianState.msg
  PedestrianStateArray.msg
  PerceptionLanes.msg
  PlannedTrajectory.msg
  PlannedTrajectoryArray.msg
  Prediction.msg
  PredictionArray.msg
  PredictionLanes.msg
  PredictionError.msg
  PredictionErrorArray.msg
  VehicleState.msg
  VehicleStateArray.msg
  Waypoint.msg
  WaypointArray.msg
  Decision.msg
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
