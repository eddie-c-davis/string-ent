cmake_minimum_required(VERSION 3.9)
project(string-ent C CXX)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -fPIC -DPIC -Xpreprocessor -ftree-vectorize -funroll-all-loops -std=c++11")

enable_testing()
add_executable(stringent ${UNIT_TESTS} ${GTEST_FILES} ${SRC_FILES})

target_link_libraries(edslTest ${LINK_LIBS})
add_test(driver StringTests)