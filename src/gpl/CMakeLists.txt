include_directories(
  ../ceres-solver/include
)

set_source_files(GPL_SRC_FILES
  CubicSpline.cc
  EigenQuaternionParameterization.cc
  gpl.cc
)

camodocal_library(camodocal_gpl SHARED ${GPL_SRC_FILES})
camodocal_link_libraries(camodocal_gpl
  ${OPENCV_CORE_LIBRARY}
  rt
)
