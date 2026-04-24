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

subdir('CMSIS')
subdir('GD32F4xx_standard_peripheral')