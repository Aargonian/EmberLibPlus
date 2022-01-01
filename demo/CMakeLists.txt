set(DEMO_SOURCES demo.cpp)

add_executable(demo EXCLUDE_FROM_ALL ${DEMO_SOURCES})
target_link_libraries(demo PRIVATE EmberLibPlus)
target_include_directories(demo PRIVATE ${EmberLibPlus_INCLUDE_DIRS})

add_custom_command(
        TARGET demo POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy ${CMAKE_CURRENT_SOURCE_DIR}/Test.txt ${CMAKE_CURRENT_BINARY_DIR}/Test.txt
        DEPENDS ${CMAKE_CURRENT_SOURCE_DIR}/Test.txt
)