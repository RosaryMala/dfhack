project(dfhack-md5)
add_library(dfhack-md5 STATIC EXCLUDE_FROM_ALL md5.cpp md5wrapper.cpp)
ide_folder(dfhack-md5 "Depends")
if(UNIX)
    set_target_properties(dfhack-md5 PROPERTIES COMPILE_FLAGS "-Wno-strict-aliasing")
endif()
