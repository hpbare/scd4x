if(ESP_PLATFORM)
    idf_component_register(
        SRCS            "scd4x.c"
        INCLUDE_DIRS    "."
    )
else()
    add_library(scd4x STATIC scd4x.c)
    target_include_directories(scd4x PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
endif()
