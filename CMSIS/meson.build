cmsis_root = include_directories('GD/GD32F4xx/Include')

cmsis_startup = []
if get_option('chip') == 'GD32F405'
    cmsis_startup += 'GD/GD32F4xx/Source/GCC/startup_gd32f405_425.S'
elif get_option('chip') == 'GD32F407'
    cmsis_startup += 'GD/GD32F4xx/Source/GCC/startup_gd32f407_427.S'
elif get_option('chip') == 'GD32F425' or get_option('chip') == 'GD32F427'
    cmsis_startup += 'GD/GD32F4xx/Source/GCC/startup_gd32f450_470.S'
elif get_option('chip') == 'GD32F450' or get_option('chip') == 'GD32F470'
    cmsis_startup += 'GD/GD32F4xx/Source/GCC/startup_gd32f450_470.S'
endif

cmsis_ld = ''
if get_option('chip') == 'GD32F405'
    cmsis_ld = 'GD/GD32F4xx/Source/GCC/Ld/gd32f405_407_xE_flash.ld'
elif get_option('chip') == 'GD32F407'
    cmsis_ld = 'GD/GD32F4xx/Source/GCC/Ld/gd32f405_407_xG_flash.ld'
elif get_option('chip') == 'GD32F425'
    cmsis_ld = 'GD/GD32F4xx/Source/GCC/Ld/gd32f425_427_xG_flash.ld'
elif get_option('chip') == 'GD32F427'
    cmsis_ld = 'GD/GD32F4xx/Source/GCC/Ld/gd32f425_427_xK_flash.ld'
elif get_option('chip') == 'GD32F450'
    cmsis_ld = 'GD/GD32F4xx/Source/GCC/Ld/gd32f450xG_flash.ld'
elif get_option('chip') == 'GD32F470'
    cmsis_ld = 'GD/GD32F4xx/Source/GCC/Ld/gd32f470xG_flash.ld'
endif

cmsis_c_args = ['-DGD32F4XX', '-D' + get_option('chip')]