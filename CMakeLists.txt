cmake_minimum_required(VERSION 3.0.2)
project(amrl_msgs)

find_package(catkin REQUIRED
  roscpp
  geometry_msgs
  sensor_msgs
  message_generation
)

## Generate messages in the 'msg' folder
add_message_files(DIRECTORY msg
  FILES
  AckermannCurvatureDriveMsg.msg
  ColoredArc2D.msg
  ColoredLine2D.msg
  ColoredPoint2D.msg
  DetectedItem.msg
  ElevatorCommand.msg
  ElevatorStatus.msg
  ErrorReport.msg
  HumanStateArrayMsg.msg
  HumanStateMsg.msg
  Localization2DMsg.msg
  PathVisualization.msg
  PlanarObjDetection.msg
  Point2D.msg
  Pose2Df.msg
  RobofleetStatus.msg
  RobofleetSubscription.msg
  VisualizationMsg.msg
)

## Generate services in the 'srv' folder
add_service_files(DIRECTORY srv
  FILES
  SocialPipsSrv.srv
)

## Generate added messages and services with any dependencies listed here
generate_messages(
  DEPENDENCIES
  std_msgs
  geometry_msgs
  sensor_msgs
)

catkin_package(
  CATKIN_DEPENDS geometry_msgs message_runtime
)