#
# Copyright (C) 2010 RobotCub Consortium
# Author: Alessandro Scalzo alessandro.scalzo@iit.it
# CopyPolicy: Released under the terms of the GNU GPL v2.0.
#

project(iCubInterfaceGuiClient)

add_definitions(${GTK2_DEFINITIONS})

file(GLOB folder_header *.h)
file(GLOB folder_source *.cpp)

include_directories(${CMAKE_PROJECT_DIR}/../iCubInterfaceGuiLib)
include_directories(${YARP_INCLUDE_DIRS})
include_directories(${iCubDev_INCLUDE_DIRS})
include_directories(${GTK2_INCLUDE_DIRS})

add_executable(${PROJECT_NAME} ${folder_source} ${folder_header})

target_link_libraries(${PROJECT_NAME} ${YARP_LIBRARIES} 
		                      ${GTK2_LIBRARIES}
                                      iCubInterfaceGuiLib)

install(TARGETS ${PROJECT_NAME} DESTINATION bin)

