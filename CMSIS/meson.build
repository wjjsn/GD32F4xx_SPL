cmsis_root = include_directories('GD/GD32F4xx/Include')
cmsis_src_root = 'GD/GD32F4xx/Source/GCC'
ldscript_path = meson.current_source_dir()/'GD'/'GD32F4xx'/'Source'/'GCC'/'Ld'
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
    'GD32F405_xE': ldscript_path/'gd32f405_407_xE_flash.ld',
    'GD32F405_xG': ldscript_path/'gd32f405_407_xG_flash.ld',
    'GD32F405_xK': ldscript_path/'gd32f405_407_xK_flash.ld',
    'GD32F407_xE': ldscript_path/'gd32f405_407_xE_flash.ld',
    'GD32F407_xG': ldscript_path/'gd32f405_407_xG_flash.ld',
    'GD32F407_xK': ldscript_path/'gd32f405_407_xK_flash.ld',
    'GD32F425_xE': ldscript_path/'gd32f425_427_xE_flash.ld',
    'GD32F425_xG': ldscript_path/'gd32f425_427_xG_flash.ld',
    'GD32F425_xK': ldscript_path/'gd32f425_427_xK_flash.ld',
    'GD32F427_xE': ldscript_path/'gd32f425_427_xE_flash.ld',
    'GD32F427_xG': ldscript_path/'gd32f425_427_xG_flash.ld',
    'GD32F427_xK': ldscript_path/'gd32f425_427_xK_flash.ld',
    'GD32F450_xE': ldscript_path/'gd32f450xE_flash.ld',
    'GD32F450_xG': ldscript_path/'gd32f450xG_flash.ld',
    'GD32F450_xK': ldscript_path/'gd32f450xK_flash.ld',
    'GD32F450_xI': ldscript_path/'gd32f450xI_flash.ld',
    'GD32F470_xE': ldscript_path/'gd32f470xE_flash.ld',
    'GD32F470_xG': ldscript_path/'gd32f470xG_flash.ld',
    'GD32F470_xK': ldscript_path/'gd32f470xK_flash.ld',
    'GD32F470_xI': ldscript_path/'gd32f470xI_flash.ld',
}

chip_option = get_option('chip')

set_variable('cmsis_root', cmsis_root)
set_variable('chip_startup', chip_startup_map[chip_option.split('_')[0]])
set_variable('chip_ldscript', chip_ld_map[chip_option])