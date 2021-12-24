
安装QT Visual Studio Tools
1. VS2017 Tools->Extensions and Updates->搜索Qt Visual Studio Tools，然后安装

2. 关于bin文件，使用windeployqt.exe 安装了必要的动态库，但是实际使用中发现版本不对或者缺少plugins文件夹，所有手动补充了库。

3. 使用CMake打开项目