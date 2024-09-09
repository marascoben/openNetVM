project('openNetVM', 'c')
add_global_arguments('-msse4', language : 'c')

cc = meson.get_compiler('c')
onvm_source = meson.current_source_dir()

# Output directory that executables are installed into
onvm_output_dir = meson.current_source_dir() + '/bin'

# ONVM configurations
onvm_mgr_app_name = 'onvm_mgr'

# DPDK dependencies
onvm_dpdk = subproject('dpdk')
onvm_dpdk_dep = onvm_dpdk.get_variable('dpdk_static_lib_deps')
onvm_dpdk_shared_dep = onvm_dpdk.get_variable('dpdk_shared_lib_deps')

# ONVM dependencies
onvm_nflib_dep = []
onvm_math_dep = cc.find_library('m')
onvm_thread_dep = dependency('threads')

# Include directories to be used when building components and examples
onvm_includes = include_directories('onvm/', 
                                    'onvm/onvm_nflib',
                                    'onvm/onvm_mgr')

# Build the ONVM components (onvm_mgr, nflib, lib)
subdir('onvm')

# Build the ONVM example apps
subdir('examples')