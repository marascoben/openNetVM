sources = files('cJSON.c')

libonvmhelper_includes = include_directories('.')

libonvmhelper = library(
    'libonvmhelper', 
    sources,
    include_directories : libonvmhelper_includes,
    install: true
)

libonvmhelper_dep = declare_dependency(
    link_with : libonvmhelper,
    include_directories: libonvmhelper_includes
)