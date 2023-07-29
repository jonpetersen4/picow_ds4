add_library(picow_ds4 
    src/bt_hid.c
)

target_include_directories(picow_ds4 PUBLIC 
    ${CMAKE_CURRENT_LIST_DIR}/src)

target_link_libraries(picow_ds4
	hardware_pwm
	hardware_gpio
	pico_stdlib
	pico_cyw43_arch_none
    pico_btstack_classic
    pico_btstack_ble
    pico_btstack_cyw43
	pico_multicore
	pico_stdio_usb
)

