sources = files(
    'main.c',
    'onvm_init.c',
    'onvm_args.c',
    'onvm_stats.c',
    'onvm_pkt.c',
    'onvm_nf.c'
)

onvm_mgr_app_name = 'onvm_mgr'

executable(onvm_mgr_app_name, 
    sources,
    include_directories: [include_directories('.'), onvm_headers, onvm_nflib_headers], 
    dependencies: [onvm_dpdk_dep, libonvmhelper_dep, libonvm_dep])