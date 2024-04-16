project('openNetVM', 'c')


cc = meson.get_compiler('c')
onvm_source = meson.current_source_dir()
onvm_dpdk = subproject('dpdk')
onvm_dpdk_dep = onvm_dpdk.get_variable('dpdk_static_lib_deps')

subdir('onvm')
