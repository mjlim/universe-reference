cmake_minimum_required(VERSION 2.6)
project(universe)

set(universe_HEADERS src/universe.h)
set(universe_SOURCES src/universe.cc src/controller.cc)

list (APPEND REQ_LIBS "")

set(CMAKE_CXX_FLAGS "-g -Wall -O3")

message (STATUS "Found OpenGL in ${OPENGL_INCLUDE_DIR}")

add_executable(universe 
    ${universe_HEADERS}
    ${universe_SOURCES}
)

target_link_libraries(universe  ${REQ_LIBS})
