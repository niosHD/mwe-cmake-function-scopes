set(VAR "SUBDIR")

function(foofunc)
  message(STATUS "Subdir Func")
  message(STATUS "VAR = ${VAR}")
endfunction()

foofunc()
