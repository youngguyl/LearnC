# For more information about build system see
# https://docs.espressif.com/projects/esp-idf/en/latest/api-guides/build-system.html
# The following five lines of boilerplate have to be in your project's
# CMakeLists in this exact order for cmake to work correctly
cmake_minimum_required(VERSION 3.16)

# 增加这行, 就不需要编译其他的库文件了
set(COMPONENTS main)

include($ENV{IDF_PATH}/tools/cmake/project.cmake)
project(learnFreeRTOS)
