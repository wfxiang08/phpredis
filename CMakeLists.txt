cmake_minimum_required(VERSION 3.2)
project(phpredis)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

INCLUDE_DIRECTORIES(
    .
    /usr/local/Cellar/php71/7.1.5_17/include/php/
    /usr/local/Cellar/php71/7.1.5_17/include/php/main
    /usr/local/Cellar/php71/7.1.5_17/include/php/Zend
)

set(SOURCE_FILES
    cluster_library.c
    cluster_library.h
    common.h
    crc16.h
    library.c
    library.h
    php_redis.h
    redis.c
    redis_array.c
    redis_array.h
    redis_array_impl.c
    redis_array_impl.h
    redis_cluster.c
    redis_cluster.h
    redis_commands.c
    redis_commands.h
    redis_session.c
    redis_session.h)

add_executable(phpredis ${SOURCE_FILES})