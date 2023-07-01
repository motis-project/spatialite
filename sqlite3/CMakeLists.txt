cmake_minimum_required(VERSION 3.10)
project(sqlite3)

add_library(libsqlite3 sqlite3.c)
target_include_directories(libsqlite3 SYSTEM PUBLIC .)
target_compile_definitions(libsqlite3 PUBLIC
  SQLITE_ENABLE_RTREE
  SQLITE_ENABLE_FTS4
  SQLITE_ENABLE_FTS5
  SQLITE_ENABLE_JSON1
  SQLITE_ENABLE_RBU
  SQLITE_ENABLE_STAT4
)
if (UNIX)
  target_link_libraries(libsqlite3 PRIVATE -ldl -lm)
endif()

add_executable(sqlite3 shell.c)
target_link_libraries(sqlite3 libsqlite3)