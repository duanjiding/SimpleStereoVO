cmake_minimum_required (VERSION 3.0)
set (CMAKE_CXX_STANDARD 11)
project(simpleVO)

find_package( OpenCV 3 REQUIRED )

add_definitions ("-Wall -std=c++11")

include_directories(
	${OpenCV_INCLUDE_DIRS}
)


add_executable(simpleVO

	main.cpp
	camera.cpp
	Frame.cpp
	camera.hpp
	Frame.hpp
	MathOperations.h
)


target_link_libraries(simpleVO
  ${OpenCV_LIBRARIES}
)
