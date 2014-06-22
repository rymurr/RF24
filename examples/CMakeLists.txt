# This configuration file outlines some of the ways Arduino CMake
# can be used. For a detailed explenation of all the options please
# reade README.rst.

set(ARDUINO_DEFAULT_BOARD diecimila) # Default Board ID, when not specified
set(ARDUINO_DEFAULT_PORT /dev/ttyUSB0) # Default Port, when not specified


# Some installations have renamed the example directories
set(PINGPAIR_SKETCH "pingpair")

link_directories(/home/ryan/workspace/RF24/RF24)
link_directories("${ARDUINO_SDK_PATH}/libraries")

set(NORDIC_SKETCH "nordic_fob")
set(PINGPAIR_SKETCH "pingpair")
set(PINGPAIRDYN_SKETCH "pingpair_dyn")
set(PINGPAIRIRQ_SKETCH "pingpair_irq")
set(PINGPAIRPL_SKETCH "pingpair_pl")
set(PINGPAIRSLEEP_SKETCH "pingpair_sleepy")
set(SCANNER_SKETCH "scanner")
set(STARPING_SKETCH "starping")

generate_arduino_firmware(nordic_fob
    SKETCH "${NORDIC_SKETCH}"
    PORT  /dev/ttyACM0
    SERIAL picocom @SERIAL_PORT@ -b 57600
    BOARD uno)

generate_arduino_firmware(pingpair
    SKETCH "${PINGPAIR_SKETCH}"
    PORT  /dev/ttyACM0
    SERIAL picocom @SERIAL_PORT@ -b 57600
    BOARD uno)

generate_arduino_firmware(pingpair_dyn
    SKETCH "${PINGPAIRDYN_SKETCH}"
    PORT  /dev/ttyACM0
    SERIAL picocom @SERIAL_PORT@ -b 57600
    BOARD uno)

generate_arduino_firmware(pingpair_irq
    SKETCH "${PINGPAIRIRQ_SKETCH}"
    PORT  /dev/ttyACM0
    SERIAL picocom @SERIAL_PORT@ -b 57600
    BOARD uno)

generate_arduino_firmware(pingpair_pl
    SKETCH "${PINGPAIRPL_SKETCH}"
    PORT  /dev/ttyACM0
    SERIAL picocom @SERIAL_PORT@ -b 57600
    BOARD uno)

generate_arduino_firmware(pingpair_sleepy
    SKETCH "${PINGPAIRSLEEP_SKETCH}"
    PORT  /dev/ttyACM0
    SERIAL picocom @SERIAL_PORT@ -b 57600
    BOARD uno)

generate_arduino_firmware(scanner
    SKETCH "${SCANNER_SKETCH}"
    PORT  /dev/ttyACM0
    SERIAL picocom @SERIAL_PORT@ -b 57600
    BOARD uno)

generate_arduino_firmware(starping
    SKETCH "${STARPING_SKETCH}"
    PORT  /dev/ttyACM0
    SERIAL picocom @SERIAL_PORT@ -b 57600
    BOARD uno)


