cmake_minimum_required(VERSION 3.12)
project(kv-store)

if(UNIX AND NOT WIN32)
    add_executable(cpp_kv_store kv-store-v1/main.c
    kv-store-v1/kvstore.c
    kv-store-v1/array.c
    kv-store-v1/rbtree.c
    kv-store-v1/btree.c
    kv-store-v1/hash.c
    kv-store-v1/dhash.c
    kv-store-v1/skiplist.c
    )
    add_executable(cpp_tb_kvstore tb_kvstore.c)
endif ()