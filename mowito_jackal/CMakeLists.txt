cmake_minimum_required(VERSION 2.8.3)
project(mowito_jackal)

find_package(catkin REQUIRED COMPONENTS roslaunch)

catkin_package()

install(
DIRECTORY launch maps params
DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
