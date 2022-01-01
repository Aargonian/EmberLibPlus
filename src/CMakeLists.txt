set(sources 
    Util/SQLite/SQLiteDB.cpp)

add_library(EmberLibPlus STATIC ${headers} ${sources})
target_include_directories(EmberLibPlus PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/../include)
