cmake_minimum_required(VERSION 3.5)

project(tracker-demo LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
SET (CMAKE_BUILD_TYPE Debug)
find_package( OpenCV REQUIRED )


include_directories( ${OpenCV_INCLUDE_DIRS} )

add_executable(tracker-demo tutorial_multitracker.cpp)
target_link_libraries(tracker-demo ${OpenCV_LIBS} )
