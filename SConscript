from building import *

group = []
if not GetDepend(['PKG_USING_NES']):
    Return('group')

cwd  = GetCurrentDir()
path = [cwd]
src	 = Glob('src/*.c')
src	 += Glob('src/mapper/*.cpp')

src	 += Glob('port/nes_embed.c')
src	 += Glob('port/nes_file_port.c')

path += [cwd + '/inc']
path += [cwd + '/src']
path += [cwd + '/port']

if not GetDepend(['PKG_NES_DFS']):
    src	 += Glob('games/*.c')

group = DefineGroup('nes', src, depend = ['PKG_USING_NES'], CPPPATH = path)

Return('group')