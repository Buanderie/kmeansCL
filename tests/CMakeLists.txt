cmake_minimum_required(VERSION 2.8)
project(KMEANSCL_TEST CXX)

# Set include directories
include_directories( ${KMEANSCL_SOURCE_DIR}/lib/include )

# Link to kmeansCL
set( DEPS "${DEPS};kmeanscl" )

file ( GLOB_RECURSE LIBKMEANSCL_TEST_CPP ./*.cc )

add_executable( kmeanscl_test ${LIBKMEANSCL_TEST_CPP} )

# Link libraries
target_link_libraries( kmeanscl_test ${DEPS} )
