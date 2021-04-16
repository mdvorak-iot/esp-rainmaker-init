cmake_minimum_required(VERSION 3.15.0)
include(ExternalComponent.cmake)

# In-place use of library in this example
list(APPEND EXTRA_COMPONENT_DIRS " ${CMAKE_SOURCE_DIR}/..")

# NOTE these dependencies are for example only, user have to include them in an actual project
ExternalComponent_Get(app_wifi https://github.com/mdvorak-iot/esp-app-wifi.git 649cc19c)
ExternalLibrary_Get(esp_rainmaker https://github.com/espressif/esp-rainmaker.git ec23bd8)
list(APPEND EXTRA_COMPONENT_DIRS ${esp_rainmaker_SOURCE_DIR}/components)

# Project
include($ENV{IDF_PATH}/tools/cmake/project.cmake)
project(esp-rainmaker-init-example)
