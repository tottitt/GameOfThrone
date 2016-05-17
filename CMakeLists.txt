cmake_minimum_required(VERSION 2.6)
project( gameOfThrone )

if( "${CMAKE_MAJOR_VERSION}.${CMAKE_MINOR_VERSION}" VERSION_GREATER "3.0")
	cmake_policy(SET CMP0053 NEW)
endif()

find_package( OpenCV REQUIRED )

ADD_DEFINITIONS(-DNDEBUG -Wall -g -c -fPIC)
ADD_EXECUTABLE(training training.cpp)
target_link_libraries(training ${OpenCV_LIBS} )


