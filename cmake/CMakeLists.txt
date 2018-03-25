cmake_minimum_required(VERSION 2.8)
project( PositioningProject )
set(OpenCV_LIBS "opencv_core;opencv_imgproc;opencv_highgui;opencv_ml;opencv_video;opencv_features2d;opencv_calib3d;opencv_objdetect")

find_package(OpenCV REQUIRED COMPONENTS core imgproc highgui)

FILE(GLOB SOURCES ../PositioningProject/src/*.cpp )
add_executable(PositioningProject ${SOURCES})
target_link_libraries(PositioningProject ${OpenCV_LIBS})

#============Debug information===============
message(STATUS "OpenCV library status:")

message(STATUS "    version: ${OpenCV_VERSION}")
message(STATUS "    libraries: ${OpenCV_LIBS}")
message(STATUS "    include path: ${OpenCV_INCLUDE_DIRS}")


#===============References==================
#https://docs.opencv.org/2.4/doc/tutorials/introduction/linux_gcc_cmake/linux_gcc_cmake.html#create-a-cmake-file
#http://answers.opencv.org/question/25642/how-to-compile-basic-opencv-program-in-c-in-ubuntu/
# Some opencv libraries have been removed in newer version

