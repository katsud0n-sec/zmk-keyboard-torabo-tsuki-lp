if(CONFIG_SHIELD_TORABO_TSUKI_LP_LEFT OR CONFIG_SHIELD_TORABO_TSUKI_LP_RIGHT)
  zephyr_library()
  zephyr_include_directories(${APPLICATION_SOURCE_DIR}/include)
  zephyr_library_sources(src/board.c)

  if(CONFIG_PAW3222)
    target_link_libraries(${PROJECT_NAME} zmk_keymap)
  endif()
endif()
