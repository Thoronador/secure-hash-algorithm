# We might support earlier versions, too, but it's only tested with 2.8.9.
cmake_minimum_required(VERSION 2.8)

# Recurse into subdirectory for sha256 executable.
add_subdirectory (sha256)

# enable tests
enable_testing()
# Recurse into subdirectory for test cases.
add_subdirectory (tests)
