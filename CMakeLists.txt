cmake_minimum_required(VERSION 3.8)
project(mqtt_srv)
set(APPNAME "mqtt_srv")

find_package(Boost REQUIRED COMPONENTS system)

find_package(Boost 1.68 REQUIRED)
find_package(mqtt_cpp_iface REQUIRED)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

add_compile_definitions(MQTT_STD_VARIANT)
add_executable(${APPNAME} main.cpp)

target_include_directories(${APPNAME} PUBLIC ${Boost_INCLUDE_DIRS}) 
target_link_libraries(${APPNAME} LINK_PUBLIC mqtt_cpp_iface::mqtt_cpp_iface)
