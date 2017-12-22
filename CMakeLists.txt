cmake_minimum_required(VERSION 3.8)
project(crazyflie_ros)

set(CMAKE_CXX_STANDARD 11)

set(SOURCE_FILES
        crazyflie_controller/src/controller.cpp
        crazyflie_controller/src/pid.hpp
        crazyflie_cpp/include/crazyflie_cpp/Crazyflie.h
        crazyflie_cpp/include/crazyflie_cpp/Crazyradio.h
        crazyflie_cpp/include/crazyflie_cpp/crtp.h
        crazyflie_cpp/src/Crazyflie.cpp
        crazyflie_cpp/src/Crazyradio.cpp
        crazyflie_demo/src/quadrotor_teleop.cpp
        crazyflie_driver/src/crazyflie_add.cpp
        crazyflie_driver/src/crazyflie_server.cpp
        crazyflie_tools/src/getParam.cpp
        crazyflie_tools/src/listLogVariables.cpp
        crazyflie_tools/src/listParams.cpp
        crazyflie_tools/src/reboot.cpp
        crazyflie_tools/src/scan.cpp)

add_executable(crazyflie_ros ${SOURCE_FILES})