set(EXE_SOURCES
    "main.cc")

add_executable(${EXECUTABLE_NAME} ${EXE_SOURCES})
target_link_libraries(${EXECUTABLE_NAME} PUBLIC
    ${LIBRARY_NAME}
    nlohmann_json
    # library name and the project name defined for this library in the related CMAKE in
    # the build/deps/specific directory of the library
    fmt::fmt
    # we could use spdlog but there is a nicer feature defined for the header only
    # header only files are faster in the CMake
    spdlog::spdlog_header_only)
