project(ev3dev-lang CXX)
cmake_minimum_required(VERSION 2.8)

set(CMAKE_CXX_FLAGS -std=c++11)

add_library(ev3dev ${CMAKE_CURRENT_SOURCE_DIR}/cpp/ev3dev.cpp)
set_target_properties(ev3dev PROPERTIES 
    PUBLIC_HEADER ${CMAKE_CURRENT_SOURCE_DIR}/cpp/ev3dev.h
)

install(TARGETS ev3dev
	PUBLIC_HEADER DESTINATION include
	ARCHIVE DESTINATION lib
	LIBRARY DESTINATION lib
)
