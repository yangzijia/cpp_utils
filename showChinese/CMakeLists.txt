cmake_minimum_required(VERSION 2.8)
project(chinese)

set(CMAKE_CXX_STANDARD 14)

find_package(OpenCV REQUIRED)
link_directories("/root/anaconda3/lib/")

#include_directories(/usr/include/freetype2/${OpenCV_INCLUDE_DIRS})

add_executable(chinese main.cpp CvxText.cpp CvxText.h)

target_link_libraries(chinese ${OpenCV_LIBS} freetype)