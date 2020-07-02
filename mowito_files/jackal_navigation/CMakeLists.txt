cmake_minimum_required(VERSION 2.8.3)
project(jackal_navigation)

find_package(catkin REQUIRED COMPONENTS roslaunch)

catkin_package()

roslaunch_add_file_check(launch/include/start_mw_mapping.launch)
roslaunch_add_file_check(launch/jackal_mw_mapping.launch)
roslaunch_add_file_check(launch/include/start_mwpfl.launch)
roslaunch_add_file_check(launch/jackal_mw_nav.launch)
roslaunch_add_file_check(launch/include/start_nav_server.launch)
roslaunch_add_file_check(launch/jackal_mw_nav_no_map.launch)
roslaunch_add_file_check(launch/include/start_costmap.launch)
roslaunch_add_file_check(launch/include/start_controller_executive.launch)
roslaunch_add_file_check(launch/include/start_explore.launch)
roslaunch_add_file_check(launch/include/start_global_planner.launch)
roslaunch_add_file_check(launch/include/start_recovery_executive.launch)
roslaunch_add_file_check(launch/include/start_rviz.launch)
roslaunch_add_file_check(launch/jackal_mw_explore_mapping.launch)


install(
DIRECTORY launch maps params
DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
