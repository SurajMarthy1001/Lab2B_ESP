cmake_minimum_required(VERSION 3.13)
project(lab_2b_p6 C CXX ASM)
set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 17)
pico_sdk_init()
add_executable(pio_logic_analyser)

# generate the header file into the source tree as it is included in the RP2040 datasheet
#pico_generate_pio_header(pio_logic_analyser ${CMAKE_CURRENT_LIST_DIR}/logic_analyser.pio OUTPUT_DIR ${CMAKE_CURRENT_LIST_DIR}/generated)

target_sources(pio_logic_analyser PRIVATE logic_analyser.c)

target_link_libraries(pio_logic_analyser PRIVATE pico_stdlib hardware_pio hardware_dma)
pico_add_extra_outputs(pio_logic_analyser)

pico_enable_stdio_usb(pio_logic_analyser 1)
pico_enable_stdio_uart(pio_logic_analyser 0)
