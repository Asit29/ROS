cmake_minimum_required(VERSION 2.8.3)
project(first_one)

find_package(catkin REQUIRED COMPONENTS
	sensor_msgs
	cv_bridge
	rospy
	std_msgs)

catkin_package(
#   INCLUDE_DIRS include
#  LIBRARIES ${PROJECT_NAME}
   CATKIN_DEPENDS rospy sensor_msgs cv_bridge std_msgs
#  DEPENDS system_lib
)


include_directories(
  include
  ${catkin_INCLUDE_DIRS}
)

catkin_install_python(PROGRAMS script.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION})
