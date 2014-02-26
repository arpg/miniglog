project(miniglog)
cmake_minimum_required(VERSION 2.8)

include(def_library)

include_directories(${CMAKE_CURRENT_SOURCE_DIR})
def_library(miniglog SOURCES miniglog/logging.h miniglog/logging.cc)
