idf_component_register(
    SRCS
        "Adafruit_GFX.cpp"
        "glcdfont.c"
        "Print.cpp"
    
    INCLUDE_DIRS
        "."
        "Fonts"

        "examples/GFXcanvas"
)

add_compile_definitions(
    ESP32_IDF
)

add_custom_command(
    OUTPUT 
        fontconvert
    
    COMMAND
        make
    
    WORKING_DIRECTORY
        ${CMAKE_CURRENT_SOURCE_DIR}/fontconvert
)
