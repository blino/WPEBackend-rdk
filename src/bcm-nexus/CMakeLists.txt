add_definitions(-DBACKEND_BCM_NEXUS=1)

list(APPEND WPE_PLATFORM_LIBRARIES
    nxpl
)

if (EGL_LIBRARIES_nxclient)
    message("-- Found NXCLIENT: TRUE [egl.pc]")
    add_definitions(-DBACKEND_BCM_NEXUS_NXCLIENT=1)
    list(APPEND WPE_PLATFORM_LIBRARIES nxclient)
endif()

list(APPEND WPE_PLATFORM_SOURCES
    src/bcm-nexus/renderer-backend.cpp
    src/bcm-nexus/view-backend.cpp
)
