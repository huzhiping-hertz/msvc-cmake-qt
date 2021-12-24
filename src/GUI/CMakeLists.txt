set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)

find_package(Qt5 COMPONENTS  Widgets REQUIRED)

set(APP_NAME "rmgui")
file(GLOB cpp_files "*.cpp")
file(GLOB ui_files "*.ui")
file(GLOB  res_files "*.qrc")
add_executable(${APP_NAME} WIN32 ${cpp_files} ${ui_files} ${res_files})
target_link_libraries(${APP_NAME}   Qt5::Widgets)
