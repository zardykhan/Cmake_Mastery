cmake_minimum_required(VERSION 3.16)

project(CppProjectTemplate VERSION 1.0.0 LANGUAGES C CXX)

#Executable is the target
add_executable(Executable main.cc)

#Add another target called LIBRARY, to include new functionality
add_library(Library STATIC my_lib.cc)

#link the library to our target
target_link_libraries(Executable PUBLIC Library)

