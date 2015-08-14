
include_directories( ${LIBKMEANSCL_SOURCE_DIR}/include )

add_executable( hello_world main.cc )

target_link_libraries( hello_world kmeanscl )

