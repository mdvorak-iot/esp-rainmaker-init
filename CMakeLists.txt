cmake_minimum_required(VERSION 3.15.0)

idf_component_register(
        SRCS src/app_rainmaker.c
        INCLUDE_DIRS include
        PRIV_REQUIRES app_update
        REQUIRES esp_rainmaker app_wifi
)
