file(GLOB COMPONENT_SRCS
    "*.cpp"
)
idf_component_register(SRCS ${COMPONENT_SRCS}
                       INCLUDE_DIRS ${CMAKE_CURRENT_LIST_DIR} $ENV{IDF_PATH}/components
                       REQUIRES console fatfs json mdns nvs_flash bt)