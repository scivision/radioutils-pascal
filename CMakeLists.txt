cmake_minimum_required (VERSION 3.0)

list(APPEND CMAKE_MODULE_PATH ${CMAKE_SOURCE_DIR}/cmake_modules)
enable_language(Pascal)
project (G4FGQ Pascal)
enable_testing()

add_executable(coax_vlf coax_vlf.pas)
add_test(NAME CoaxVLF COMMAND bash -c "./coax_vlf <<< q")
set_tests_properties(CoaxVLF PROPERTIES PASS_REGULAR_EXPRESSION "Program name: COAX_VLF")

add_executable(grndwav3 grndwav3.pas)
add_test(NAME GroundWave COMMAND bash -c "./grndwav3 <<< q")
set_tests_properties(GroundWave PROPERTIES PASS_REGULAR_EXPRESSION "Program name: GRNDWAV3")

add_executable(line_zin line_zin.pas)
add_test(NAME LineImpedance COMMAND bash -c "./line_zin <<< q")
set_tests_properties(LineImpedance PROPERTIES PASS_REGULAR_EXPRESSION "Program name: LINE_ZIN")

add_executable(padmatch padmatch.pas)
add_test(NAME PadMatch COMMAND bash -c "./padmatch <<< q")
set_tests_properties(PadMatch PROPERTIES PASS_REGULAR_EXPRESSION "Program name: PADMATCH")

add_executable(propgate propgate.pas)
add_test(NAME Propagate COMMAND bash -c "./propgate <<< q")
set_tests_properties(Propagate PROPERTIES PASS_REGULAR_EXPRESSION "Program name: PROPGATE")

add_executable(tophat2 tophat2.pas)
add_test(NAME TopHat COMMAND bash -c "./tophat2 <<< e")
set_tests_properties(TopHat PROPERTIES PASS_REGULAR_EXPRESSION "Program name: TOPHAT2")

add_executable(tranco_1 tranco_1.pas)
add_test(NAME TransCoil COMMAND bash -c "./tranco_1 <<< q")
set_tests_properties(TransCoil PROPERTIES PASS_REGULAR_EXPRESSION "Program name: TRANCO_1")

