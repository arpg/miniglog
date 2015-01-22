project(MINIGLOG)
cmake_minimum_required(VERSION 2.8)

list(APPEND CMAKE_MODULE_PATH ${CMAKE_CURRENT_SOURCE_DIR}/CMakeModules)
include(def_library)
include(export_package)

set(USER_INC ${CMAKE_CURRENT_SOURCE_DIR}) # Variable used for config export
include_directories(${USER_INC})

option(BUILD_SHARED_LIBS "Build Shared Library" ON)
set(LIBRARY_NAME miniglog)
def_library(${LIBRARY_NAME}
  SOURCES miniglog/logging.h miniglog/logging.cc
  PACKAGE MINIGLOG
  )

export_package(MINIGLOG
  TARGETS miniglog
  INCLUDE_DIRS ${USER_INC}
  LIBRARY miniglog
  LIBRARIES miniglog
  )
