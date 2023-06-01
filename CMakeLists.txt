cmake_minimum_required(VERSION 3.10)
project(hpipm_opti_ctr_demos CXX)
set(CMAKE_CXX_STANDARD 11)

find_package(Eigen3 REQUIRED)
find_package(hpipm-cpp REQUIRED)


add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/src)

