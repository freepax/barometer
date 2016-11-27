cmake_minimum_required (VERSION 2.6)
project (BAROMETER)

set(CMAKE_CURRENT_SOURCE_DIR .)

SET(CMAKE_INSTALL_RPATH_USE_LINK_PATH TRUE)
set(CMAKE_INSTALL_PREFIX /usr/)

set(BAROMETER-SOURCE
  barometer.cpp
)

add_executable(barometer ${BAROMETER-SOURCE})
target_link_libraries(barometer firmware_i2c ssd1306 bmp180)

install(TARGETS barometer DESTINATION bin)
