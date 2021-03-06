
cmake_minimum_required(VERSION 2.8.3)
project(cob_voltage_control)

find_package(catkin REQUIRED COMPONENTS roscpp libphidgets cob_relayboard rospy dynamic_reconfigure)

###################################
## Dynamic reconfigure ##
###################################
generate_dynamic_reconfigure_options(cfg/cob_voltage_control.cfg)


###################################
## catkin specific configuration ##
###################################
catkin_package(
    CATKIN_DEPENDS roscpp libphidgets cob_relayboard rospy dynamic_reconfigure
    INCLUDE_DIRS 
    LIBRARIES 
)

###########
## Build ##
###########
# add include search paths
include_directories(common/src ${Boost_INCLUDE_DIRS} ${catkin_INCLUDE_DIRS})


add_executable(cob_voltage_control ros/src/cob_voltage_control_ros.cpp)
target_link_libraries(cob_voltage_control ${catkin_LIBRARIES}) 


#############
## Install ##
#############

## Mark executables and/or libraries for installation
install(TARGETS cob_voltage_control
  ARCHIVE DESTINATION ${CATKIN_PACKAGE_LIB_DESTINATION}
  LIBRARY DESTINATION ${CATKIN_PACKAGE_LIB_DESTINATION}
  RUNTIME DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)

## Mark cpp header files for installation
install(DIRECTORY ros/launch/
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/ros/launch
)

install(PROGRAMS ros/src/record_current.py ros/src/record_voltage.py ros/src/savitzky.py ros/src/savitzky_golay.py ros/src/time_volt.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)
