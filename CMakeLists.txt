cmake_minimum_required(VERSION 3.3)

project(boost_winapi)

add_library(boost_winapi INTERFACE)

target_include_directories(boost_winapi BEFORE INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/include)

install(TARGETS boost_winapi DESTINATION lib)
install(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/include/boost DESTINATION include)

add_library(boost::winapi ALIAS boost_winapi)
