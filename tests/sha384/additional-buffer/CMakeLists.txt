# We might support earlier versions, too, but it's only tested with 2.8.9.
cmake_minimum_required (VERSION 2.8)

# binary for additional SHA-384 buffer tests
project(test_additional_buffer_sha384)

set(test_additional_buffer_sha384_src
    ../../../libstriezel/hash/sha384/BufferSourceUtility.cpp
    ../../../libstriezel/hash/sha384/sha384.cpp
    ../../../libstriezel/hash/sha512/BufferSource.cpp
    ../../../libstriezel/hash/sha512/MessageSource.cpp
    main.cpp)

# We use a C++11 feature in the code, so enable C++0x a.k.a. C++11.
add_definitions(-Wall -O2 -fexceptions -std=c++0x)

set( CMAKE_EXE_LINKER_FLAGS  "${CMAKE_EXE_LINKER_FLAGS} -s" )

add_executable(test_additional_buffer_sha384 ${test_additional_buffer_sha384_src})

# add it as a test
add_test(NAME SHA-384-additional-buffer
         COMMAND $<TARGET_FILE:test_additional_buffer_sha384> --long)
