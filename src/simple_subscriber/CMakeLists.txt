cmake_minimum_required(VERSION 2.8.3)
project(simple_subscriber)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  std_msgs
)

catkin_package(
)

include_directories(
  include
  ${catkin_INCLUDE_DIRS}
)

add_executable(simple_subscriber src/subscriber.cpp src/subscriber_node.cpp)
target_link_libraries(simple_subscriber ${catkin_LIBRARIES})
