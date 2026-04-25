project('GD32F4xx_Firmware', 'c', version: '3.3.3')

option_chip = get_option('chip')
option_time = get_option('time')

if option_chip == ''
    error('chip option must be specified by user: meson setup -Dchip=GD32F407 <source_dir>')
endif

time_map = {
    'irc16m': 'IRC16M',
    'hxtal': 'HXTAL',
    '120m_irc16m': '120M_PLL_IRC16M',
    '120m_8m_hxtal': '120M_PLL_8M_HXTAL',
    '120m_25m_hxtal': '120M_PLL_25M_HXTAL',
    '168m_irc16m': '168M_PLL_IRC16M',
    '168m_8m_hxtal': '168M_PLL_8M_HXTAL',
    '168m_25m_hxtal': '168M_PLL_25M_HXTAL',
    '200m_irc16m': '200M_PLL_IRC16M',
    '200m_8m_hxtal': '200M_PLL_8M_HXTAL',
    '200m_25m_hxtal': '200M_PLL_25M_HXTAL',
    '240m_irc16m': '240M_PLL_IRC16M',
    '240m_8m_hxtal': '240M_PLL_8M_HXTAL',
    '240m_25m_hxtal': '240M_PLL_25M_HXTAL',
}

global_args = ['-mcpu=cortex-m4', '-mthumb', '-mfpu=fpv4-sp-d16', '-mfloat-abi=hard',
               '-DGD32F4XX', '-D' + option_chip, '-D__SYSTEM_CLOCK_' + time_map[option_time]]

add_project_arguments(global_args, language: 'c')

chip_option = get_option('chip')
chip_family = chip_option.split('_')[0]

ldscript_path = 'CMSIS'/'GD'/'GD32F4xx'/'Source'/'GCC'/'Ld'

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

chip_startup_map = {
    'GD32F405': ['CMSIS'/'GD'/'GD32F4xx'/'Source'/'GCC'/'startup_gd32f405_425.S', 'CMSIS'/'GD'/'GD32F4xx'/'Source'/'system_gd32f4xx.c'],
    'GD32F407': ['CMSIS'/'GD'/'GD32F4xx'/'Source'/'GCC'/'startup_gd32f407_427.S', 'CMSIS'/'GD'/'GD32F4xx'/'Source'/'system_gd32f4xx.c'],
    'GD32F425': ['CMSIS'/'GD'/'GD32F4xx'/'Source'/'GCC'/'startup_gd32f405_425.S', 'CMSIS'/'GD'/'GD32F4xx'/'Source'/'system_gd32f4xx.c'],
    'GD32F427': ['CMSIS'/'GD'/'GD32F4xx'/'Source'/'GCC'/'startup_gd32f407_427.S', 'CMSIS'/'GD'/'GD32F4xx'/'Source'/'system_gd32f4xx.c'],
    'GD32F450': ['CMSIS'/'GD'/'GD32F4xx'/'Source'/'GCC'/'startup_gd32f450_470.S', 'CMSIS'/'GD'/'GD32F4xx'/'Source'/'system_gd32f4xx.c'],
    'GD32F470': ['CMSIS'/'GD'/'GD32F4xx'/'Source'/'GCC'/'startup_gd32f450_470.S', 'CMSIS'/'GD'/'GD32F4xx'/'Source'/'system_gd32f4xx.c'],
}

periph_src = [
    'GD32F4xx_standard_peripheral'/'Source'/'gd32f4xx_adc.c',
    'GD32F4xx_standard_peripheral'/'Source'/'gd32f4xx_can.c',
    'GD32F4xx_standard_peripheral'/'Source'/'gd32f4xx_crc.c',
    'GD32F4xx_standard_peripheral'/'Source'/'gd32f4xx_ctc.c',
    'GD32F4xx_standard_peripheral'/'Source'/'gd32f4xx_dac.c',
    'GD32F4xx_standard_peripheral'/'Source'/'gd32f4xx_dbg.c',
    'GD32F4xx_standard_peripheral'/'Source'/'gd32f4xx_dci.c',
    'GD32F4xx_standard_peripheral'/'Source'/'gd32f4xx_dma.c',
    'GD32F4xx_standard_peripheral'/'Source'/'gd32f4xx_enet.c',
    'GD32F4xx_standard_peripheral'/'Source'/'gd32f4xx_exmc.c',
    'GD32F4xx_standard_peripheral'/'Source'/'gd32f4xx_exti.c',
    'GD32F4xx_standard_peripheral'/'Source'/'gd32f4xx_fmc.c',
    'GD32F4xx_standard_peripheral'/'Source'/'gd32f4xx_fwdgt.c',
    'GD32F4xx_standard_peripheral'/'Source'/'gd32f4xx_gpio.c',
    'GD32F4xx_standard_peripheral'/'Source'/'gd32f4xx_i2c.c',
    'GD32F4xx_standard_peripheral'/'Source'/'gd32f4xx_ipa.c',
    'GD32F4xx_standard_peripheral'/'Source'/'gd32f4xx_iref.c',
    'GD32F4xx_standard_peripheral'/'Source'/'gd32f4xx_misc.c',
    'GD32F4xx_standard_peripheral'/'Source'/'gd32f4xx_pmu.c',
    'GD32F4xx_standard_peripheral'/'Source'/'gd32f4xx_rcu.c',
    'GD32F4xx_standard_peripheral'/'Source'/'gd32f4xx_rtc.c',
    'GD32F4xx_standard_peripheral'/'Source'/'gd32f4xx_sdio.c',
    'GD32F4xx_standard_peripheral'/'Source'/'gd32f4xx_spi.c',
    'GD32F4xx_standard_peripheral'/'Source'/'gd32f4xx_syscfg.c',
    'GD32F4xx_standard_peripheral'/'Source'/'gd32f4xx_timer.c',
    'GD32F4xx_standard_peripheral'/'Source'/'gd32f4xx_tli.c',
    'GD32F4xx_standard_peripheral'/'Source'/'gd32f4xx_trng.c',
    'GD32F4xx_standard_peripheral'/'Source'/'gd32f4xx_usart.c',
    'GD32F4xx_standard_peripheral'/'Source'/'gd32f4xx_wwdgt.c',
]

all_src = chip_startup_map[chip_family] + periph_src

gd32f4xx_spl_inc = include_directories(
    'GD32F4xx_standard_peripheral'/'Include',
    'CMSIS'/'GD'/'GD32F4xx'/'Include',
    'CMSIS',
)

GD32F4xx_SPL_dep = declare_dependency(
    include_directories: gd32f4xx_spl_inc,
    sources: all_src,
    compile_args: ['-D' + chip_family],
    link_args: ['-T', chip_ld_map[chip_option]],
)
