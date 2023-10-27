# EffekseerForCocos2d-x
Effekseer runtime for Cocos2d-x v3 compatible with editor 1.53e

Install in cocos2d-x project:

    git submodule add https://github.com/WuJiayiSH/EffekseerForCocos2d-x-v3.git frameworks\EffekseerForCocos2d-x-v3

Update your CMakeLists.txt:

    add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/frameworks/EffekseerForCocos2d-x-v3)
    target_link_libraries(${APP_NAME} effekseer)
    target_include_directories(${APP_NAME} PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/frameworks/EffekseerForCocos2d-x-v3)
