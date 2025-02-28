#[[ 这是一个 CMakeLists.txt 文件。
这是一个 CMakeLists.txt 文件
这是一个 CMakeLists.txt 文件]]
cmake_minimum_required(VERSION 3.0)
project(CALC)
# add_executable(app add.c div.c main.c mult.c sub.c)
set(SRC_LIST add.cpp;div.cpp;main.cpp;mult.cpp;sub.cpp)

#增加-std=c++11
set(CMAKE_CXX_STANDARD 11)
#增加-std=c++14
set(CMAKE_CXX_STANDARD 14)
#增加-std=c++17
set(CMAKE_CXX_STANDARD 17)

#[[
在CMake中指定可执行程序输出的路径，
也对应一个宏，叫做EXECUTABLE_OUTPUT_PATH，
它的值还是通过set命令进行设置:
]]#
set(HOME )
set(EXECUTABLE_OUTPUT_PATH ${HOME}/bin)


add_executable(app  ${SRC_LIST})