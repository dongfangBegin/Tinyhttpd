CMAKE_MINIMUM_REQUIRED(VERSION 3.8)
project(main)

## aux_source_directory(httpd.c HTTDPD_SRC)
add_executable(httpd httpd.c)
target_compile_options(httpd PRIVATE -g -W -Wall)
target_link_libraries(httpd pthread)

## aux_source_directory(simpleclient.c CLIENT_SRC)
add_executable(client simpleclient.c)
target_link_libraries(client PRIVATE gcc)
target_compile_options(client PRIVATE -g -W -Wall)
