# 0) create code and CMake File
# 1) mkdir build (because it is common practive to create a build directory to place all the stuff there)
# 2) cd build
# 3) cmake .. (the .. means the reference for the directory one lvl above the build folder.)
# 4) cmake --build (this command tells the cmkake not to configure but to build the configured traget)
# 5) ./Executable make sure you are in the file
cmake_minimum_required(VERSION 3.16)

project(CppProjectTemplate VERSION 1.0.0 LANGUAGES C CXX)
#always look at the cmake tool suggestions for the arguements
#the string between < > is just to be filled without <>

#this is a target
add_executable(Executable main.cc)
