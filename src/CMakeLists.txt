find_library(VOROLIB voro++ /usr/local/lib)
include_directories(/usr/local/include/voro++)
set (CMAKE_CXX_FLAGS "-O3 -std=gnu++11")
file (GLOB _sources *.c*)
add_executable(se_api ${_sources})
target_link_libraries (se_api ${VOROLIB} boost_program_options)

