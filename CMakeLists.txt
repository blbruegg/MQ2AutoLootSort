# MQ2AutoLootSort
# Forked from RedGuides/MQ2AutoLootSort (github.com/RedGuides org sweep, forum-plugins-2026-08-02
# follow-up batch). Vendored as a git submodule tracking https://github.com/blbruegg/MQ2AutoLootSort
# (fork of RedGuides/MQ2AutoLootSort). See F:\\EQProject\\docs\\re_progress.md for the write-up.

include("../../Plugin.cmake")

set(MQ2AutoLootSort_SOURCES
    "LootSort.cpp"
    "LootSort.h"
    "MQ2AutoLootSort.cpp"
)

source_groups("Source Files" ${MQ2AutoLootSort_SOURCES})

add_library(MQ2AutoLootSort SHARED
    ${MQ2AutoLootSort_SOURCES}
)

set_target_properties(MQ2AutoLootSort PROPERTIES FOLDER "core/plugins")

target_Plugin_props(MQ2AutoLootSort)

target_link_libraries(MQ2AutoLootSort PRIVATE MQ2Main)
