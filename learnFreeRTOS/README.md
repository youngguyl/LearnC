# 在 linux 上模拟 FreeRTOS 实验环境

## 参考连接

- [在Linux上运行 freeRTOS 实验](https://docs.espressif.com/projects/esp-idf/zh_CN/stable/esp32/api-guides/host-apps.html)

## 操作步骤

1. 安装 libbsd-dev 包：`sudo apt-get install libbsd-dev`
2. 修改 项目/CMakeLists.txt 文件，添加以下内容：
```cmake
cmake_minimum_required(VERSION 3.16)

# 增加这行, 就不需要编译其他的库文件了
set(COMPONENTS main)
include($ENV{IDF_PATH}/tools/cmake/project.cmake)
project(learnFreeRTOS)
```
3. 设置目标板：`idf.py --preview set-target linux`
4. 编译查看项目：`idf.py build monitor`
4. 如果需要切换回 esp32 目标板，则执行：`idf.py set-target esp32`