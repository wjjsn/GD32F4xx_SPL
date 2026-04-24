cmsis_root = include_directories('GD/GD32F4xx/Include')
cmsis_src_root = 'GD/GD32F4xx/Source/GCC'
system_src = 'GD/GD32F4xx/Source/system_gd32f4xx.c'

chip_src_map = {
    'GD32F405': [cmsis_src_root + '/startup_gd32f405_425.S', system_src],
    'GD32F407': [cmsis_src_root + '/startup_gd32f407_427.S', system_src],
    'GD32F425': [cmsis_src_root + '/startup_gd32f405_425.S', system_src],
    'GD32F427': [cmsis_src_root + '/startup_gd32f407_427.S', system_src],
    'GD32F450': [cmsis_src_root + '/startup_gd32f450_470.S', system_src],
    'GD32F470': [cmsis_src_root + '/startup_gd32f450_470.S', system_src],
}

chip_ld_map = {
    'GD32F405': cmsis_src_root + '/Ld/gd32f405_407_xE_flash.ld',
    'GD32F407': cmsis_src_root + '/Ld/gd32f405_407_xG_flash.ld',
    'GD32F425': cmsis_src_root + '/Ld/gd32f425_427_xG_flash.ld',
    'GD32F427': cmsis_src_root + '/Ld/gd32f425_427_xK_flash.ld',
    'GD32F450': cmsis_src_root + '/Ld/gd32f450xG_flash.ld',
    'GD32F470': cmsis_src_root + '/Ld/gd32f470xG_flash.ld',
}

<<<<<<< HEAD
cmsis_lib = static_library('gd32f4xx_cmsis', chip_src_map[get_option('chip')],
                           include_directories: cmsis_root)

gd32f4xx_cmsis_dep = declare_dependency(link_with: cmsis_lib,
                                        include_directories: cmsis_root,
                                        variables: {'ldscript': chip_ld_map[get_option('chip')]})
=======
set_variable('cmsis_root', cmsis_root)
set_variable('chip_startup', chip_startup_map[get_option('chip')])
set_variable('chip_ldscript', chip_ld_map[get_option('chip')])
>>>>>>> main
