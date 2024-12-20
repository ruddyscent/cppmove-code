file(GLOB SOURCES "*.cpp")

foreach(SOURCE ${SOURCES})
    get_filename_component(EXECUTABLE_NAME ${SOURCE} NAME_WE)
    add_executable(${EXECUTABLE_NAME} ${SOURCE})

    if(${SOURCE} MATCHES "movenoexcept.cpp")
        target_compile_definitions(${EXECUTABLE_NAME} PRIVATE NOEXCEPT=noexcept)
    endif()

endforeach()

