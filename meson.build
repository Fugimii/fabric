project('fabric', 'c', version: '0.0.1')

if build_machine.system() == 'windows'
    error('fabric is not meant for windows users, consider moving to linux.')
endif

pymod = import('python')
python = pymod.find_installation(
  'python3',
  modules: [
    'gi',
    'cairo',
    'loguru',
    'click',
  ],
)

if python.language_version().version_compare('<3.8')
    error('at least Python 3.8 is required, Python 3.11 is recommended though.')
endif

dependency('cairo')
dependency('gtk+-3.0')
dependency('py3cairo')
dependency('pygobject-3.0')
dependency('cairo-gobject')
dependency('gtk-layer-shell-0')
dependency('gobject-introspection-1.0')

