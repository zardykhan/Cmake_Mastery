#we use the ${LIBRARY_NAME} variable that we have defined in the upper-most CMakeLists
add_library(${LIBRARY_NAME} STATIC my_lib.cc)
target_include_directories(${LIBRARY_NAME} PUBLIC "./")
