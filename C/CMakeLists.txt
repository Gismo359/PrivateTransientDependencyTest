project(C)

add_library(C SHARED c.c)

target_link_libraries(C PRIVATE B)

foreach(dir IN LISTS $<TARGET_RUNTIME_DLL_DIRS:C>)
    message(STATUS "Runtime DLL directory: ${dir}")
endforeach()
