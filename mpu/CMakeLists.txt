cmake_minimum_required(VERSION 3.13)

include(pico_sdk_import.cmake)

project(mpu6050_i2c_project)

pico_sdk_init()



add_executable(mpu6050_i2c
    mpu6050_i2c.c
)

pico_enable_stdio_usb(mpu6050_i2c 1)

pico_enable_stdio_uart(mpu6050_i2c 1)

pico_add_extra_outputs(mpu6050_i2c)



target_link_libraries(mpu6050_i2c pico_stdlib hardware_i2c)
