# EffekseerForCocos2d-x
Effekseer runtime for Cocos2d-x v3 compatible with editor 1.53e

Install in cocos2d-x project:

    git submodule add https://github.com/WuJiayiSH/EffekseerForCocos2d-x-v3.git frameworks\EffekseerForCocos2d-x-v3

Update your CMakeLists.txt:

    include_directories(${CMAKE_CURRENT_SOURCE_DIR}/frameworks/EffekseerForCocos2d-x-v3)
    include(${CMAKE_CURRENT_SOURCE_DIR}/frameworks/EffekseerForCocos2d-x-v3/CMakeLists.txt)
    set(GAME_HEADER ${GAME_HEADER} ${EFFEKSEER_HEADER})
    set(GAME_SOURCE ${GAME_SOURCE} ${EFFEKSEER_SRC})
