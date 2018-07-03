valacounter_sources = [
  'main.vala',
  'window.vala',
]

valacounter_deps = [
  dependency('gio-2.0', version: '>= 2.50'),
  dependency('gtk+-3.0', version: '>= 3.22'),
]

gnome = import('gnome')

valacounter_sources += gnome.compile_resources('valacounter-resources',
  'valacounter.gresource.xml',
  c_name: 'valacounter'
)

executable('valacounter', valacounter_sources,
  vala_args: '--target-glib=2.50',  dependencies: valacounter_deps,
  install: true,
)
