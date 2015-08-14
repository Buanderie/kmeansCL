cmake_minimum_required(VERSION 2.8 FATAL_ERROR)
project(LIBKMEANSCL CXX)

# Set custom cmake scripts directory
set( CMAKE_MODULE_PATH "${CMAKE_MODULE_PATH};${LIBKMEANSCL_SOURCE_DIR}/cmake")

# Set include directories
include_directories( ${LIBKMEANSCL_SOURCE_DIR}/include )

file ( GLOB_RECURSE CORE_CPP ./src/*.cc )
set( LIBKMEANSCL_CPP ${CORE_CPP} )
add_library( kmeanscl SHARED ${LIBKMEANSCL_CPP} )

# Link libraries
target_link_libraries( kmeanscl ${DEPS} )
