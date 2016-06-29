cmake_minimum_required(VERSION 2.8.3)
project(drake_ros)

find_package(catkin REQUIRED COMPONENTS roscpp)

catkin_package(
  INCLUDE_DIRS include
  #LIBRARIES
  #CATKIN_DEPENDS
  #DEPENDS
)

catkin_add_gtest(ros_test test/ros_test.cc)
#target_link_libraries(ros_test ${catkin_LIBRARIES})
#add_test(NAME ros_test COMMAND ros_test)

install(DIRECTORY include/${PROJECT_NAME}/
        DESTINATION ${CATKIN_PACKAGE_INCLUDE_DESTINATION}
        FILES_MATCHING PATTERN "*.h")
