cmake_minimum_required(VERSION 2.8.3)
project(copernicus_simulation)

add_compile_options(-std=c++11)

find_package(catkin REQUIRED COMPONENTS 
	roslaunch
	velodyne_gazebo_plugins
	pointcloud_to_laserscan
	velodyne_description
)


catkin_package()

roslaunch_add_file_check(launch)

include_directories()

 install(
   DIRECTORY launch worlds
   DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
 )

