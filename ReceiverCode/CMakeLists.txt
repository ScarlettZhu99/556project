cmake_minimum_required(VERSION 3.10)
project(ReceiverCode)

set(CMAKE_CXX_STANDARD 11)

include_directories(.)

add_executable(ReceiverCode
        "Collect script"
        pip_sense.v2
        pip_sense_layer.v2.cpp
        sample_data.hpp
        sensor_aggregator_protocol.hpp
        simple_sockets.hpp)
