cmake_minimum_required(VERSION 3.10)
project(gtsam_examples)

# if you see a segfault: https://groups.google.com/forum/#!topic/gtsam-users/sDNbMiCtRYI
find_package(GTSAM REQUIRED) # Uses installed package
include_directories(${GTSAM_INCLUDE_DIR})
link_directories(${GTSAM_LIBRARY_DIRS})

#find_package(Boost REQUIRED)
#include_directories(${Boost_INCLUDE_DIR})

add_executable(ISAM2_SmartFactorStereo_IMU ISAM2_SmartFactorStereo_IMU.cpp)
target_link_libraries(ISAM2_SmartFactorStereo_IMU gtsam)
