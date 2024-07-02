project(rmod_launcher)

#find required packages
find_package(waifulib REQUIRED)

# Name of executable
set(EXECNAME main)
#Source files
set(SRC 
  launcher_main/main.cpp
)
include_directories(${CMAKE_SOURCE_DIR} 
 launcher 
 launcher_main 
 sdklauncher
)
#Create Executable
add_executable(${EXECNAME} ${SRC})
#Link Libraries
target_link_libraries(${EXECNAME})