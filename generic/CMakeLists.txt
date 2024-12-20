file(GLOB SOURCES "*.cpp")

# Remove files that are coded to intentionally generate an error
list(REMOVE_ITEM SOURCES
    "${CMAKE_CURRENT_SOURCE_DIR}/universalclass.cpp"
    "${CMAKE_CURRENT_SOURCE_DIR}/universalmem.cpp")

foreach(SOURCE ${SOURCES})
    get_filename_component(EXECUTABLE_NAME ${SOURCE} NAME_WE)
    add_executable(${EXECUTABLE_NAME} ${SOURCE})
endforeach()
