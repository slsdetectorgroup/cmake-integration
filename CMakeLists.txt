cmake_minimum_required(VERSION 3.14)
project(myintegration)

find_package(slsDetectorPackage 8.0 REQUIRED)
add_executable(example main.cpp)
target_link_libraries(example slsDetectorShared)
