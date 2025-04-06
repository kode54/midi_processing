cmake_minimum_required(VERSION 3.14)

project(
    midi_processing
    VERSION 0.1.0
    DESCRIPTION "MIDI file parser and converter library"
    HOMEPAGE_URL "https://github.com/kode54/midi_processing"
    LANGUAGES CXX
)
set(target midi_processing)
add_library(${target} STATIC ${sources})

target_include_directories(${target} PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}")

target_sources(${target} PUBLIC
midi_container.cpp
midi_container.h
midi_processor_gmf.cpp
midi_processor_helpers.cpp
midi_processor_hmi.cpp
midi_processor_hmp.cpp
midi_processor_lds.cpp
midi_processor_mids.cpp
midi_processor_mus.cpp
midi_processor_riff_midi.cpp
midi_processor_standard_midi.cpp
midi_processor_syx.cpp
midi_processor_xmi.cpp
midi_processor.h)