cmake_minimum_required(VERSION 3.19)
project(WebServer)

set(CMAKE_CXX_STANDARD 14)

include_directories(code/buffer)
include_directories(code/config)
include_directories(code/http)
include_directories(code/log)
include_directories(code/pool)
include_directories(code/server)
include_directories(code/timer)

add_executable(WebServer
        code/buffer/buffer.cpp
        code/buffer/buffer.h
        code/config/config.h
        code/http/httpconn.cpp
        code/http/httpconn.h
        code/http/httprequest.cpp
        code/http/httprequest.h
        code/http/httpresponse.cpp
        code/http/httpresponse.h
        code/log/blockqueue.h
        code/log/log.cpp
        code/log/log.h
        code/pool/sqlconnpool.cpp
        code/pool/sqlconnpool.h
        code/pool/sqlconnRAII.h
        code/pool/threadpool.h
        code/server/epoller.cpp
        code/server/epoller.h
        code/server/webserver.cpp
        code/server/webserver.h
        code/timer/heaptimer.cpp
        code/timer/heaptimer.h
        code/main.cpp
        webbench-1.5/socket.c
        webbench-1.5/webbench.c)
