# CMakeList.txt : Top-level CMake project file, do global configuration
# and include sub-projects here.
#
cmake_minimum_required (VERSION 3.10)
project ("RMGUI")

#set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

#QT msvc 编译器安装目录
set(CMAKE_PREFIX_PATH C:/Qt/Qt5.14.2/5.14.2/msvc2017_64)


#头文件搜索路径
INCLUDE_DIRECTORIES(${PROJECT_SOURCE_DIR}/external/include)
INCLUDE_DIRECTORIES(${PROJECT_SOURCE_DIR}/src)

#链接库搜索路径
#这个用于Release版本
LINK_DIRECTORIES(${PROJECT_SOURCE_DIR}/external/lib)


#执行文件输出路径
SET(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)
#库文件输出路径
SET(LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)

#项目源码
add_subdirectory(src)
