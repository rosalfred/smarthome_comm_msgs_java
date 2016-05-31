##############################################################################
# CMake
##############################################################################

cmake_minimum_required(VERSION 2.8.3)
project(smarthome_comm_msgs_java)

##############################################################################
# Catkin
##############################################################################

find_package(catkin REQUIRED
    rosjava_build_tools
    smarthome_comm_msgs)

# Set the gradle targets you want catkin's make to run by default, e.g.
#   catkin_rosjava_setup(installApp)
# Note that the catkin_create_rosjava_xxx scripts will usually automatically
# add tasks to this for you when you create subprojects.
catkin_rosjava_setup(publishMavenJavaPublicationToMavenRepository)

catkin_package()

##############################################################################
# Installation
##############################################################################

# Change this to match the maven group name you have specified in the
# allprojects closure the root build.gradle
install(DIRECTORY ${CATKIN_DEVEL_PREFIX}/${CATKIN_GLOBAL_MAVEN_DESTINATION}/org/ros/rosjava_messages/smarthome_comm_msgs/
        DESTINATION ${CATKIN_GLOBAL_MAVEN_DESTINATION}/org/ros/rosjava_messages/smarthome_comm_msgs)
