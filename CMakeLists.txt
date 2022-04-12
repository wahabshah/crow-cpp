cmake_minimum_required(VERSION 3.7.2)

project(crow-servers)

find_package(Crow)
add_executable(crow-server crow-server.cpp)
target_link_libraries(crow-server PUBLIC Crow::Crow)