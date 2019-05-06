cmake_minimum_required(VERSION 3.10)
project(PIPtagCode)

set(CMAKE_CXX_STANDARD 11)

include_directories(PIPtagCode)
include_directories(PIPtagCode/CC110x)
include_directories(PIPtagCode/Owl)
include_directories(PIPtagCode/sensing)
include_directories(ReceiverCode)

add_executable(PIPtagCode
        PIPtagCode/CC110x/CC1100-CC2500.c
        PIPtagCode/CC110x/CC1100-CC2500.h
        PIPtagCode/CC110x/definitions.h
        PIPtagCode/CC110x/rfsuite.c
        PIPtagCode/CC110x/rfsuite.h
        PIPtagCode/CC110x/TI_CC_CC1100-CC2500.h
        PIPtagCode/CC110x/TI_CC_hardware_board_2553.h
        PIPtagCode/CC110x/TI_CC_msp430.h
        PIPtagCode/CC110x/TI_CC_spi.c
        PIPtagCode/CC110x/TI_CC_spi.h
        PIPtagCode/CC110x/tuning.c
        PIPtagCode/CC110x/tuning.h
        PIPtagCode/Owl/history.c
        PIPtagCode/Owl/history.h
        PIPtagCode/Owl/mem_pool.c
        PIPtagCode/Owl/mem_pool.h
        PIPtagCode/sensing/battery.c
        PIPtagCode/sensing/battery.h
        PIPtagCode/sensing/htu21d.c
        PIPtagCode/sensing/htu21d.h
        PIPtagCode/sensing/light.c
        PIPtagCode/sensing/light.h
        PIPtagCode/sensing/moisture.c
        PIPtagCode/sensing/moisture.h
        PIPtagCode/sensing/sensing.c
        PIPtagCode/sensing/sensing.h
        PIPtagCode/sensing/temperature.c
        PIPtagCode/sensing/temperature.h
        PIPtagCode/floatToBits.cpp
        PIPtagCode/interrupt.c
        PIPtagCode/interrupt.h
        PIPtagCode/main.c
        PIPtagCode/main.h
        PIPtagCode/optical_conn.c
        PIPtagCode/optical_conn.h
        PIPtagCode/settings.h
        ReceiverCode/pip_sense_layer.v2.cpp
        ReceiverCode/sample_data.hpp
        ReceiverCode/sensor_aggregator_protocol.hpp
        ReceiverCode/simple_sockets.hpp)
