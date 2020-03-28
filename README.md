# Dragon-bones demo version  
---  
Briefly, It's code used to show a working demo with [dragon bones](https://github.com/DragonBones/DragonBonesCPP/tree/dev).  
  
It's adapted to [cocos2dx v4.0](https://github.com/cocos2d/cocos2d-x/tree/cocos2d-x-4.0)
- add cmake support
- easy to integrate into the cocos2dx project. Just modify root CMakeLists.txt in the created project   
```cmake
# compile and link dragonbones lib
set(DRAGONBONES_ROOT_PATH Classes/own-extension/dragonBones)
add_subdirectory(${DRAGONBONES_ROOT_PATH})

target_link_libraries(${APP_NAME} PUBLIC cocos2d dragon_bones )

target_include_directories(${APP_NAME}
    PRIVATE Classes
    PRIVATE ${DRAGONBONES_ROOT_PATH}/.. 					#this line was added
    PRIVATE ${COCOS2DX_ROOT_PATH}/cocos/audio/include/
)
```