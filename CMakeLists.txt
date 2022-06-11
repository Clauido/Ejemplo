cmake_minimum_required(VERSION 3.0.0)
project(intento VERSION 0.1.0)

include(CTest)
enable_testing()

find_package( OpenCV REQUIRED)
include_directories(${Opencv_INCLUDE_DIRS})
include_directories("includes")

add_executable(intento main.cpp)

target_link_libraries( intento ${OpenCV_LIBS})

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
