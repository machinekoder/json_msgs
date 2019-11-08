cmake_minimum_required(VERSION 2.8.3)
project(json_msgs)
add_definitions(-std=c++11)

find_package(catkin REQUIRED COMPONENTS message_generation std_msgs)

add_message_files(FILES JsonData.msg)

add_service_files(FILES JsonService.srv)

generate_messages(DEPENDENCIES std_msgs)

catkin_package(CATKIN_DEPENDS message_runtime std_msgs)
