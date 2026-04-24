cmsis_root = include_directories('GD/GD32F4xx/Include')
cmsis_src_root = 'GD/GD32F4xx/Source/GCC'

chip_startup_map = {
    'GD32F405_xE': cmsis_src_root + '/startup_gd32f405_425.S',
    'GD32F405_xG': cmsis_src_root + '/startup_gd32f405_425.S',
    'GD32F405_xK': cmsis_src_root + '/startup_gd32f405_425.S',
    'GD32F407_xE': cmsis_src_root + '/startup_gd32f407_427.S',
    'GD32F407_xG': cmsis_src_root + '/startup_gd32f407_427.S',
    'GD32F407_xK': cmsis_src_root + '/startup_gd32f407_427.S',
    'GD32F425_xE': cmsis_src_root + '/startup_gd32f405_425.S',
    'GD32F425_xG': cmsis_src_root + '/startup_gd32f405_425.S',
    'GD32F425_xK': cmsis_src_root + '/startup_gd32f405_425.S',
    'GD32F427_xE': cmsis_src_root + '/startup_gd32f407_427.S',
    'GD32F427_xG': cmsis_src_root + '/startup_gd32f407_427.S',
    'GD32F427_xK': cmsis_src_root + '/startup_gd32f407_427.S',
    'GD32F450_xE': cmsis_src_root + '/startup_gd32f450_470.S',
    'GD32F450_xG': cmsis_src_root + '/startup_gd32f450_470.S',
    'GD32F450_xK': cmsis_src_root + '/startup_gd32f450_470.S',
    'GD32F450_xI': cmsis_src_root + '/startup_gd32f450_470.S',
    'GD32F470_xE': cmsis_src_root + '/startup_gd32f450_470.S',
    'GD32F470_xG': cmsis_src_root + '/startup_gd32f450_470.S',
    'GD32F470_xK': cmsis_src_root + '/startup_gd32f450_470.S',
    'GD32F470_xI': cmsis_src_root + '/startup_gd32f450_470.S',
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

gd32f4xx_cmsis_dep = declare_dependency(include_directories: cmsis_root,
                                        variables: {'startup': chip_startup_map[get_option('chip')],
                                                   'ldscript': chip_ld_map[get_option('chip')]})