cmake_minimum_required(VERSION 3.10)
# set the project name
project(HelloProj VERSION 1.0)
#export configuration to source code
configure_file(HelloProjConfig.h.in HelloProjConfig.h)
#add the executable target named HelloWorld
add_executable(HelloWorld hello.cpp)

# add binary tree to the list of paths to search includes
target_include_directories(HelloWorld
 PUBLIC "${PROJECT_BINARY_DIR}")