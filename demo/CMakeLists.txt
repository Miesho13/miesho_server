cmake_minimum_required(VERSION 3.22)

set(projectName server_demo)
project(${projectName})


include(../src/miesho_server.cmake)
add_library(miesho_server STATIC ${MIESHO_SERVER_LIB_SRC})


add_executable(${projectName} main.c)
target_link_libraries(${projectName} miesho_server)