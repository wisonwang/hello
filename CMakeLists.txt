project(main)
cmake_minimum_required(VERSION 2.6)

set(TARGET_NAME main)
set(TYPE "")

set( CPP_SOURCES
  main.cpp
  )

set( H_SOURCES
  main.hpp
  )

set(SOURCES
  ${CPP_SOURCES}
  ${H_SOURCES}
  )

set(INC
  ${CMAKE_CURRENT_SOURCE_DIR}
  )

include_directories(${INC})

if(UNIX)
  add_definitions(-Wno-write-strings)
endif()

add_executable(${TARGET_NAME} ${TYPE} ${SOURCES})

set(LIBS
  )

target_link_libraries(${TARGET_NAME} ${LIBS})
target_link_libraries
