set(MODULE_NAME EncodeMeasurementsSR)

#-----------------------------------------------------------------------------
set(MODULE_SRCS
  ${MODULE_NAME}.cxx
  )

#-----------------------------------------------------------------------------
set(MODULE_TARGET_LIBRARIES
  ${DCMTK_LIBRARIES}
  xml2 z
  )

#-----------------------------------------------------------------------------
SEMMacroBuildCLI(
  NAME ${MODULE_NAME}
  INCLUDE_DIRECTORIES ${MODULE_INCLUDE_DIRECTORIES}  
  ADDITIONAL_SRCS ${MODULE_SRCS}
  TARGET_LIBRARIES ${MODULE_TARGET_LIBRARIES}  
  RUNTIME_OUTPUT_DIRECTORY        "${CMAKE_RUNTIME_OUTPUT_DIRECTORY}"
  LIBRARY_OUTPUT_DIRECTORY        "${CMAKE_LIBRARY_OUTPUT_DIRECTORY}"
  ARCHIVE_OUTPUT_DIRECTORY        "${CMAKE_ARCHIVE_OUTPUT_DIRECTORY}"
  INSTALL_RUNTIME_DESTINATION ${CMAKE_BINARY_DIR}
  INSTALL_LIBRARY_DESTINATION ${CMAKE_BINARY_DIR}
  INSTALL_ARCHIVE_DESTINATION ${CMAKE_BINARY_DIR}
  )


