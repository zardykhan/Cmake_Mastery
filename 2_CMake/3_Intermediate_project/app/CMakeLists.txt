#we use the ${EXECUTALBE_NAME} variable that we have defined in the upper-most CMakeLists
add_executable(${EXECUTABLE_NAME} main.cc)
target_link_libraries(${EXECUTABLE_NAME} PUBLIC Library)
