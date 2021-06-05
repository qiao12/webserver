cmake_minimum_required(VERSION 3.19)
project(WebServer)

set(CMAKE_CXX_STANDARD 14)

include_directories(code/src/buffer)
include_directories(code/src/config)
include_directories(code/src/http)
include_directories(code/src/log)
include_directories(code/src/pool)
include_directories(code/src/server)
include_directories(code/src/timer)

add_executable(WebServer
        code/src/buffer/buffer.cpp
        code/include/buffer/buffer.h
        code/src/config/config.h
        code/src/http/httpconn.cpp
        code/include/http/httpconn.h
        code/src/http/httprequest.cpp
        code/include/http/httprequest.h
        code/src/http/httpresponse.cpp
        code/include/http/httpresponse.h
        code/include/log/blockqueue.h
        code/src/log/log.cpp
        code/include/log/log.h
        code/src/pool/sqlconnpool.cpp
        code/include/pool/sqlconnpool.h
        code/include/pool/sqlconnRAII.h
        code/include/pool/threadpool.h
        code/src/server/epoller.cpp
        code/include/server/epoller.h
        code/src/server/webserver.cpp
        code/include/server/webserver.h
        code/src/timer/heaptimer.cpp
        code/include/timer/heaptimer.h
        code/main.cpp
        webbench-1.5/socket.c
        webbench-1.5/webbench.c)
