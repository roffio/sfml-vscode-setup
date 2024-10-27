cmake_minimum_required(VERSION 3.10)

project(MySFMLProject LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

include_directories("${CMAKE_SOURCE_DIR}/SFML-2.6.1/include")

add_executable(main src/main.cpp)

target_link_libraries(main 
    "${CMAKE_SOURCE_DIR}/SFML-2.6.1/lib/sfml-graphics.lib"
    "${CMAKE_SOURCE_DIR}/SFML-2.6.1/lib/sfml-window.lib"
    "${CMAKE_SOURCE_DIR}/SFML-2.6.1/lib/sfml-system.lib"
)

set_target_properties(main PROPERTIES OUTPUT_NAME "main")
