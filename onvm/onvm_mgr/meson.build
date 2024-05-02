sources = files(
    'main.c',
    'onvm_args.c',
    'onvm_init.c',
    'onvm_nf.c',
    'onvm_pkt.c',
    'onvm_stats.c'
)

onvm_mgr_app_name = 'onvm_mgr'

onvm_mgr_include = include_directories('.')

executable(onvm_mgr_app_name, 
    sources,
    include_directories: [onvm_mgr_include, onvm_headers, onvm_nflib_headers], 
    dependencies: [onvm_dpdk_shared_dep, libonvm_dep, libonvmhelper_dep, onvm_math_dep],
)