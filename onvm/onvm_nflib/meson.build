sources = files(
    'onvm_config_common.c',
    'onvm_flow_dir.c',
    'onvm_flow_table.c',
    'onvm_nflib.c',
    'onvm_pkt_common.c',
    'onvm_pkt_helper.c',
    'onvm_sc_common.c',
    'onvm_sc_mgr.c',
    'onvm_threading.c'
)

libonvm = static_library('libonvm', 
    sources, 
    include_directories : include_directories('.'),
    dependencies : [onvm_dpdk_dep, libonvmhelper_dep])
libonvm_dep = declare_dependency(link_with: libonvm)