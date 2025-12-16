idf_component_register(
    SRCS
        "app_main.cpp"
        "app_driver.cpp"
    PRIV_INCLUDE_DIRS
        "."
        "${ESP_MATTER_PATH}/examples/common/utils"
    PRIV_REQUIRES
        esp_matter
        nvs_flash
        driver
)

# Optional: include certification declaration (if enabled)
if (CONFIG_ENABLE_SET_CERT_DECLARATION_API)
    target_add_binary_data(${COMPONENT_TARGET}
        "certification_declaration/certification_declaration.der" BINARY)
endif()

# Required for Matter config compatibility
target_compile_options(${COMPONENT_LIB} PRIVATE "-DCHIP_HAVE_CONFIG_H")

