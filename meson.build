project('openNetVM', 'c')
add_global_arguments('-msse4', language : 'c')

cc = meson.get_compiler('c')
onvm_source = meson.current_source_dir()
onvm_dpdk = subproject('dpdk', default_options: ['mssse3=true'])
onvm_dpdk_dep = onvm_dpdk.get_variable('dpdk_static_lib_deps')

subdir('onvm')
