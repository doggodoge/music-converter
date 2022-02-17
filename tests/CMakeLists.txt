include(FetchContent)
FetchContent_Declare(
        googletest
        URL https://github.com/google/googletest/archive/0e402173c97aea7a00749e825b194bfede4f2e45.zip
)
# For Windows: Prevent overriding the parent project's compiler/linker settings
set(gtest_force_shared_crt ON CACHE BOOL "" FORCE)
FetchContent_MakeAvailable(googletest)

enable_testing()

add_executable(
        music-converter-test
	empty_tests.test.cpp
)
# TODO: Add this back in when we have a testing library
# add_dependencies(parallel-factorial-test parallel-factorial-lib)
target_link_libraries(
        music-converter-test
	# TODO: Uncomment when we actually have a lib.
	# music-converter-lib
        gtest_main
)
