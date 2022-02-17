find_package(Threads REQUIRED)

set(
        SOURCE
        main.cpp
)
add_executable(
        music-converter
        ${SOURCE}
)
target_link_libraries(
        music-converter
        Threads::Threads
)
# TODO: Add this later when we've got something real to add.
# add_library(music-converter-lib STATIC parallel_factorial.cpp parallel_factorial.h)
