cmsis_root = include_directories('GD/GD32F4xx/Include')
cmsis_src_root = 'GD/GD32F4xx/Source/GCC'
system_src = 'GD/GD32F4xx/Source/system_gd32f4xx.c'

chip_startup_map = {
    'GD32F405': [cmsis_src_root + '/startup_gd32f405_425.S', system_src],
    'GD32F407': [cmsis_src_root + '/startup_gd32f407_427.S', system_src],
    'GD32F425': [cmsis_src_root + '/startup_gd32f405_425.S', system_src],
    'GD32F427': [cmsis_src_root + '/startup_gd32f407_427.S', system_src],
    'GD32F450': [cmsis_src_root + '/startup_gd32f450_470.S', system_src],
    'GD32F470': [cmsis_src_root + '/startup_gd32f450_470.S', system_src],
}

chip_ld_map = {
    'GD32F405_xE': cmsis_src_root + '/Ld/gd32f405_407_xE_flash.ld',
    'GD32F405_xG': cmsis_src_root + '/Ld/gd32f405_407_xG_flash.ld',
    'GD32F405_xK': cmsis_src_root + '/Ld/gd32f405_407_xK_flash.ld',
    'GD32F407_xE': cmsis_src_root + '/Ld/gd32f405_407_xE_flash.ld',
    'GD32F407_xG': cmsis_src_root + '/Ld/gd32f405_407_xG_flash.ld',
    'GD32F407_xK': cmsis_src_root + '/Ld/gd32f405_407_xK_flash.ld',
    'GD32F425_xE': cmsis_src_root + '/Ld/gd32f425_427_xE_flash.ld',
    'GD32F425_xG': cmsis_src_root + '/Ld/gd32f425_427_xG_flash.ld',
    'GD32F425_xK': cmsis_src_root + '/Ld/gd32f425_427_xK_flash.ld',
    'GD32F427_xE': cmsis_src_root + '/Ld/gd32f425_427_xE_flash.ld',
    'GD32F427_xG': cmsis_src_root + '/Ld/gd32f425_427_xG_flash.ld',
    'GD32F427_xK': cmsis_src_root + '/Ld/gd32f425_427_xK_flash.ld',
    'GD32F450_xE': cmsis_src_root + '/Ld/gd32f450xE_flash.ld',
    'GD32F450_xG': cmsis_src_root + '/Ld/gd32f450xG_flash.ld',
    'GD32F450_xK': cmsis_src_root + '/Ld/gd32f450xK_flash.ld',
    'GD32F450_xI': cmsis_src_root + '/Ld/gd32f450xI_flash.ld',
    'GD32F470_xE': cmsis_src_root + '/Ld/gd32f470xE_flash.ld',
    'GD32F470_xG': cmsis_src_root + '/Ld/gd32f470xG_flash.ld',
    'GD32F470_xK': cmsis_src_root + '/Ld/gd32f470xK_flash.ld',
    'GD32F470_xI': cmsis_src_root + '/Ld/gd32f470xI_flash.ld',
}

chip_option = get_option('chip')

set_variable('cmsis_root', cmsis_root)
set_variable('chip_startup', chip_startup_map[chip_option.split('_')[0]])
set_variable('chip_ldscript', chip_ld_map[chip_option])