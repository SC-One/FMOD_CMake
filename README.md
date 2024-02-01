# FMOD_CMake
Making fmod available using as submodule in CMake based projects 

## How
Just add these lines to the parent project's cmake file (please be careful about the paths).
```
set(FMOD_HOME "/the address of the fmod libraries")
set(CMAKE_MODULE_PATH ${FMOD_CMake_FOLDER_I_MEAN_THIS_FOLDER})
find_package(FMOD MODULE REQUIRED)
target_link_libraries($PARENT_TARGET_PRJ ${FMOD_LIBRARY_LIB})
target_include_directories($PARENT_TARGET_PRJ PUBLIC ${FMOD_INCLUDE_DIR} include)
```
