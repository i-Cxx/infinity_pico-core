add_library(blink_lib STATIC
    Blink.cpp
    blink_task_wrapper.cpp
)

target_include_directories(blink_lib PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}
)

target_link_libraries(blink_lib
    pico_stdlib
    hardware_gpio
    freertos          
)