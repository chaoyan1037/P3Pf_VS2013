cmake_minimum_required (VERSION 2.6)

project (p3pf)

# modify this according to your PC
set( EIGEN_INCLUDE_DIR "D:/eigen" )

# add our macro directory to cmake search path
if (EXISTS "${CMAKE_SOURCE_DIR}/cmake")
  set (CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} ${CMAKE_SOURCE_DIR}/cmake)
endif ()

include("${CMAKE_MODULE_PATH}/OptimizeCompilerFlags.cmake")
OptimizeCompilerFlags()

add_subdirectory (ext)
add_subdirectory (src)
