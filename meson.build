project('openNetVM', 'c')
add_global_arguments('-msse4', language : 'c')

cc = meson.get_compiler('c')
onvm_source = meson.current_source_dir()

# DPDK dependency instantiation
onvm_dpdk = subproject('dpdk')
onvm_dpdk_dep = onvm_dpdk.get_variable('dpdk_static_lib_deps')

# Header directories to search when building components
onvm_headers = include_directories('onvm/')
onvm_nflib_headers = include_directories('onvm/onvm_nflib/')

# Builds meson.build files found within onvm/
subdir('onvm')
