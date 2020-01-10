gdb调试cmake工程  [参考链接](https://blog.csdn.net/lemonaha/article/details/72837561)

在cmakelist.txt中添加
'''
SET(CMAKE_BUILD_TYPE "Debug")
SET(CMAKE_CXX_FLAGS_DEBUG "$ENV{CXXFLAGS} -O0 -Wall -g -ggdb")
SET(CMAKE_CXX_FLAGS_RELEASE "$ENV{CXXFLAGS} -O3 -Wall")
'''
在工程目录新建build
'''
cd build
cmake .. -DCMAKE_BUILD_TYPE=Dubug
make
'''
进入调试
'''
gdb exe_file_name
'''
