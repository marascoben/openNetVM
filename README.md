# [openNetVM][onvm]

> _Please let us know if you use OpenNetVM in your research by [emailing us](mailto:timwood@gwu.edu) or completing this [short survey](https://goo.gl/forms/oxcnGO45Kxq1Zyyi2)._

> _Want to get started quickly?_ Try using our NSF CloudLab profile: <https://www.cloudlab.us/p/GWCloudLab/onvm>

openNetVM is a high performance NFV platform based on [DPDK][dpdk] and [Docker][docker] containers.  openNetVM provides a flexible framework for deploying network functions and interconnecting them to build service chains.

openNetVM is an open source version of the NetVM platform described in our [NSDI 2014][nsdi14] and [HotMiddlebox 2016][hotmiddlebox16] papers, released under the [BSD][license] license.  

The [develop][dev] branch tracks experimental builds (active development) whereas the [master][mast] branch tracks verified stable releases.  Please read our [releases][rels] document for more information about our releases and release cycle.

You can find information about research projects building on [OpenNetVM][onvm] at the [UCR/GW SDNFV project site][sdnfv]. OpenNetVM is supported in part by NSF grants CNS-1422362 and CNS-1522546.

## Getting Started

We've provided a bash script to assist with setting up your development environment for working with OpenNetVM. Take a look at [`scripts/setup.sh`](/scripts/setup.sh) to see a full list of installed packages.

From the `openNetVM` folder, run the following two commands:

```text
./scripts/setup.sh
```

```text
sudo ./scripts/setup_runtime.sh
```

### Building

OpenNetVM uses the [Meson][meson] build system to compile all components, including dpdk. From the `openNetVM` parent folder run the following to setup build:

```text
meson build
```

Then, `cd` into the build folder and run ninja to compile:

```text
cd ./build
ninja
```

### Running onvm_mgr

After finishing build, from the build directory, you can run the `install` command to place the compiled executables in ther source directories.

```text
meson install
```

Then, you can use our provided startup script to launch onvm_mgr. This scripts assumes the `openNetVM` folder is your working directory.

```text
./scripts/startup.sh
```

## Usage Guide

### Sample NFs

openNetVM comes with several sample NFs. To get started with these, check out the [examples guide][examples].

### Creating NFs

We have created an [NF development guide][nfs] to provide you with steps to create your first NF.

### Containerizing NFs

NFs can be run inside docker containers, with the NF being automatically or hand started. For more informations, see our [Docker guide][docker-nf].

### mTCP apps as NFs

openNetVM can run mTCP applications as NFs. For more information, visit [mTCP][mtcp].

## Citing

If you use OpenNetVM in your work, please cite our paper:

```text
@inproceedings{zhang_opennetvm:_2016,
 title = {{OpenNetVM}: {A} {Platform} for {High} {Performance} {Network} {Service} {Chains}},
 booktitle = {Proceedings of the 2016 {ACM} {SIGCOMM} {Workshop} on {Hot} {Topics} in {Middleboxes} and {Network} {Function} {Virtualization}},
 publisher = {ACM},
 author = {Zhang, Wei and Liu, Guyue and Zhang, Wenhui and Shah, Neel and Lopreiato, Phillip and Todeschi, Gregoire and Ramakrishnan, K.K. and Wood, Timothy},
 month = aug,
 year = {2016},
}
```

>_Please let us know if you use OpenNetVM in your research by [emailing us](mailto:timwood@gwu.edu) or completing this [short survey](https://goo.gl/forms/oxcnGO45Kxq1Zyyi2)._

[onvm]: http://sdnfv.github.io/onvm/
[sdnfv]: http://sdnfv.github.io/
[license]: LICENSE
[dpdk]: http://dpdk.org
[docker]: https://www.docker.com/
[nsdi14]: http://faculty.cs.gwu.edu/timwood/papers/14-NSDI-netvm.pdf
[hotmiddlebox16]: http://faculty.cs.gwu.edu/timwood/papers/16-HotMiddlebox-onvm.pdf
[examples]: https://opennetvm.readthedocs.io/en/develop/examples/index.html
[nfs]: https://opennetvm.readthedocs.io/en/develop/nfdev/index.html
[docker-nf]: https://opennetvm.readthedocs.io/en/develop/docker/index.html
[dev]: https://github.com/sdnfv/openNetVM/tree/develop
[mast]: https://github.com/sdnfv/openNetVM/tree/master
[rels]: docs/Releases.md
[mtcp]: https://github.com/eunyoung14/mtcp
[meson]: https://mesonbuild.com/
