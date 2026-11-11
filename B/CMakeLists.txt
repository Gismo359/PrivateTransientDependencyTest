project(B)

add_library(B SHARED b.c)

target_link_libraries(B PRIVATE A)