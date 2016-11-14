cmake_minimum_required(VERSION 3.1.0)

project(func-scope)

set(VAR "MAINDIR")

function(foofunc)
  message(STATUS "Maindir Func")
  message(STATUS "VAR = ${VAR}")
endfunction()

foofunc() 

add_subdirectory(subdir)

foofunc()
