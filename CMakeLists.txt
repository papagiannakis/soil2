cmake_minimum_required(VERSION 2.8.3)
project(soil2 C)

include(cmake/Findsoil2.cmake)

include_directories(${soil2_INCLUDE_DIR})

file(GLOB SOURCES
    "${CMAKE_CURRENT_LIST_DIR}/src/SOIL2/*.c"
    "${CMAKE_CURRENT_LIST_DIR}/src/SOIL2/*.h"
	"${CMAKE_CURRENT_LIST_DIR}/include/*.h")

add_library(${soil2_LIBRARY} STATIC ${SOURCES})
