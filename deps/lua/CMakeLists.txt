AUX_SOURCE_DIRECTORY(${CMAKE_CURRENT_SOURCE_DIR}/src SOURCE_LIST)

ADD_LIBRARY(lua ${SOURCE_LIST})
TARGET_INCLUDE_DIRECTORIES(lua PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/inc)
SET_SOURCE_FILES_PROPERTIES(./src/lgc.c PROPERTIES COMPILE_FLAGS -w)
SET_SOURCE_FILES_PROPERTIES(./src/ltable.c PROPERTIES COMPILE_FLAGS -w)
SET_SOURCE_FILES_PROPERTIES(./src/loslib.c PROPERTIES COMPILE_FLAGS -w)
