# This configuration file outlines some of the ways Arduino CMake
# can be used. For a detailed explenation of all the options please
# reade README.rst.

set(ARDUINO_DEFAULT_BOARD diecimila) # Default Board ID, when not specified
set(ARDUINO_DEFAULT_PORT /dev/ttyUSB0) # Default Port, when not specified


# Some installations have renamed the example directories
set(PINGPAIR_SKETCH "pingpair")

#generate_arduino_library(RF24
#    SRCS ../RF24/RF24.cpp
#    HDRS ../RF24/RF24.h ../RF24/nRF24L01.h
#    LIBS SPI
#    BOARD uno)
link_directories(/home/ryan/workspace/RF24/RF24)
link_directories("${ARDUINO_SDK_PATH}/libraries")

generate_arduino_firmware(pingpair
    SKETCH "${PINGPAIR_SKETCH}"
    PORT  /dev/ttyACM0
    SERIAL picocom @SERIAL_PORT@ -b 57600
    BOARD uno)


#====================================================================#
# Advanced firwmare example
#====================================================================#
#generate_arduino_firmware(blink
#    SRCS blink.cpp
#    LIBS blink_lib
#    BOARD uno)
