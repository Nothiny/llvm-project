add_object_library(
  time_utils
  SRCS
    time_utils.cpp
  HDRS
    time_utils.h
  DEPENDS
    libc.hdr.types.clock_t
    libc.hdr.time_macros
)

add_object_library(
  clock_gettime
  SRCS
    clock_gettime.cpp
  HDRS
    ../clock_gettime.h
  DEPENDS
    libc.hdr.types.clockid_t
    libc.hdr.types.struct_timespec
    .time_utils
)
