# Create a library called "myLib2" (in Linux, this library is created
# with the name of either libmyLib2.a or myLib2.so).
find_package(OpenCV REQUIRED)
add_library (myLib2
  # list of cpp source files:
  src.cpp
  )

# Indicate what directories should be added to the include file search
# path when using this library.
target_include_directories(myLib2 PUBLIC
  # list of directories:
  .
  ${OpenCV_INCLUDE_DIRS}
  )

  target_link_libraries(myLib2
  ${OpenCV_LIBS}
  )
