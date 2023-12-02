cmake_minimum_required(VERSION 3.26)
project(sdl_test)

set(CMAKE_CXX_STANDARD 17)

include_directories(${PROJECT_SOURCE_DIR}/Libs/sdl/include)

add_executable(${PROJECT_NAME} main.cpp)

find_library(LIBSDL2 SDL2 ${PROJECT_SOURCE_DIR}/Libs/sdl/lib)
target_link_libraries(${PROJECT_NAME} ${LIBSDL2})

configure_file(${PROJECT_SOURCE_DIR}/Libs/sdl/bin/SDL2.dll ${CMAKE_CURRENT_BINARY_DIR} COPYONLY)