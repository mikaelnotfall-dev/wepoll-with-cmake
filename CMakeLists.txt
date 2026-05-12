cmake_minimum_required(VERSION 3.10)
project(wepoll LANGUAGES C)

add_library(wepoll STATIC wepoll.c wepoll.h)

target_include_directories(wepoll PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
target_link_libraries(wepoll PRIVATE ws2_32 mswsock)
