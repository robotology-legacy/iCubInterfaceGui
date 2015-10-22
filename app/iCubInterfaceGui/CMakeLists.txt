# Copyright: (C) 2015 iCub Facility Istituto Italiano di Tecnologia
# Authors: Alessandro Scalzo
# CopyPolicy: Released under the terms of the GNU GPL v2.0.

file(GLOB icon_files ${CMAKE_CURRENT_SOURCE_DIR}/icons/*.png)
yarp_install(FILES ${icon_files} DESTINATION ${ICUBCONTRIB_CONTEXTS_INSTALL_DIR}/iCubInterfaceGui/icons)



