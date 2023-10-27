set(LIB_NAME effekseer)

include_directories(
    ${CMAKE_CURRENT_SOURCE_DIR}
    ${COCOS2DX_ROOT_PATH}/cocos
    ${COCOS2DX_ROOT_PATH}/cocos/base
    ${COCOS2DX_ROOT_PATH}/cocos/platform
    ${COCOS2DX_ROOT_PATH}/external
    ${COCOS2DX_ROOT_PATH}/external/glfw3/include/win32
)

if(WINDOWS)
    include_directories(${COCOS2DX_ROOT_PATH}/external/win32-specific/gles/include/OGLES)
endif()

file(GLOB_RECURSE EFFEKSEER_SRC 
    ${CMAKE_CURRENT_LIST_DIR}/Effekseer/Effekseer.cpp
    ${CMAKE_CURRENT_LIST_DIR}/Effekseer/EffekseerNative.cpp
    ${CMAKE_CURRENT_LIST_DIR}/Effekseer/EffekseerRendererNative.cpp
)

file(GLOB_RECURSE EFFEKSEER_HEADER 
    ${CMAKE_CURRENT_LIST_DIR}/Effekseer/Effekseer.h
    ${CMAKE_CURRENT_LIST_DIR}/Effekseer/EffekseerNative.h
    ${CMAKE_CURRENT_LIST_DIR}/Effekseer/EffekseerRendererNative.h
)

add_library(${LIB_NAME} STATIC ${EFFEKSEER_SRC} ${EFFEKSEER_HEADER})
add_dependencies(${LIB_NAME} cocos2d)
use_cocos2dx_compile_define(${LIB_NAME})