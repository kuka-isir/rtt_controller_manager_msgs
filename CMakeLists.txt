cmake_minimum_required(VERSION 2.8.3)
project(rtt_controller_manager_msgs)

find_package(catkin REQUIRED COMPONENTS rtt_roscomm controller_manager_msgs)

ros_generate_rtt_typekit(controller_manager_msgs)
ros_generate_rtt_service_proxies(controller_manager_msgs)

orocos_generate_package(
  DEPENDS controller_manager_msgs
  DEPENDS_TARGETS rtt_roscomm  rtt_std_msgs

)
