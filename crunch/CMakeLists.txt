add_executable(crunch_exe
	corpus_gen.cpp
	corpus_test.cpp
	crunch.cpp
)

target_include_directories(crunch_exe
  PUBLIC ${CMAKE_SOURCE_DIR}/inc
)

target_link_libraries(crunch_exe
	PUBLIC crunch
)

set_target_properties(crunch_exe
  PROPERTIES
  OUTPUT_NAME crunch)

install(TARGETS crunch_exe DESTINATION bin)
