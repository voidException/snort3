
set(FILE_LIST
    arp_spoof.cc
    arp_module.cc
    arp_module.h
)

if (STATIC_INSPECTORS)
    add_library(arp_spoof STATIC
        ${FILE_LIST}
    )

else (STATIC_INSPECTORS)
    add_shared_library(arpspoof inspectors ${FILE_LIST})
    
endif (STATIC_INSPECTORS)
