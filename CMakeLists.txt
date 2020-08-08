cmake_minimum_required(VERSION 3.0.0)
project(LA1002 VERSION 0.1.0)

include(CTest)
enable_testing()


# 查找当前目录下的所有源文件
# 并将名称保存到 DIR_SRCS 变量
aux_source_directory(. DIR_SRCS)

# 指定生成目标
add_executable(LA1002 ${DIR_SRCS})

# 增加math.h标准库
target_link_libraries(${PROJECT_NAME} m)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
