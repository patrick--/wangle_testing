set(LIBRARIES
        wangle fizz folly gflags glog pthread
        dl aio boost_context boost_program_options
        boost_thread boost_filesystem boost_system boost_regex
        boost_chrono bz2 c dwarf elf ssl crypto
        lzma z snappy lz4 iberty event double-conversion
        sodium jemalloc unwind
)

add_executable(client EchoClient.cpp )
add_executable(server EchoServer.cpp )

target_link_libraries(client ${LIBRARIES})