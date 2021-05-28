cmake_minimum_required(VERSION 3.4.1)
project(dbnet-onnxrun-cpp)

find_package(OpenCV REQUIRED)
set(onnxruntime_INCLUDE_DIRS /opt/onnxruntime-linux-x64-1.6.0/include)
include_directories(${onnxruntime_INCLUDE_DIRS})

include_directories(${OpenCV_INCLUDE_DIRS})
add_executable(dbnet-onnxrun-cpp main.cpp)
target_link_libraries(dbnet-onnxrun-cpp ${OpenCV_LIBS} /opt/onnxruntime-linux-x64-1.6.0/lib/libonnxruntime.so)
set_property(TARGET dbnet-onnxrun-cpp PROPERTY CXX_STANDARD 14)
