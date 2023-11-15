cmake_minimum_required(VERSION 3.14)
project(YourProjectName)

# Include the GoogleTest directory (adjust the path as necessary)
add_subdirectory(googletest)

# Add the GoogleTest header files
include_directories(googletest/googletest/include)

# Define your test executable
add_executable(your_test_executable gs.cpp)

# Link the Google Test libraries
target_link_libraries(your_test_executable gtest gtest_main)

# Enable testing using Google Test
enable_testing()
add_test(NAME your_test_executable COMMAND your_test_executable)

