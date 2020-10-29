add_executable (rope-test test.cpp)
target_link_libraries (rope-test PRIVATE rope UnitTest++)
add_test (NAME test-rope COMMAND $<TARGET_FILE:rope-test>)
