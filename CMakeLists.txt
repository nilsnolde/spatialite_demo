cmake_minimum_required (VERSION 3.12)
project (spatialite_test LANGUAGES CXX C)

include(${CMAKE_SOURCE_DIR}/cmake/FindSpatiaLite.cmake)
include(${CMAKE_SOURCE_DIR}/cmake/FindSQLite3.cmake)

add_executable(spatialite_demo ${CMAKE_SOURCE_DIR}/demo1.c)

target_link_libraries(spatialite_demo PUBLIC SpatiaLite::SpatiaLite SQLite3::SQLite3)
