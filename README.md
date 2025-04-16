# README

Supporting functionality for ansible work with KVM/QEMU virtual machines.

## References:

- [Open Issue driving this work](https://github.com/ansible-collections/community.libvirt/issues/148)
- [One variant for kvm provisioning](https://github.com/Tronde/kvm_provision_lab/tree/main)
- [Redhat blog post for a fast lab creation](https://www.redhat.com/en/blog/build-VM-fast-ansible)

## Overview:

During an exercise with the fast lab deployment (published as fast as  36 seconds execution time) of a KVM , the following completion anomaly was observed.

1. The vm template was referring to an existing vm storage file.
2. Other more recent work, see references, offered parameterized storage file locations.
3. Each discussion seems to have always presumed an existing set of storage devs, virtio.
4. Even where creation/initialization of storage (and subsequent OS attributes)  was addressed, templates were not , or were not, minimal. 

In other words, given the minimal set of parameters to configure a storage device/volume for kvm deployments to successfully build on a host machine,  **  is there an equivalent minimal template  ** that has less work to modify than the templates used in the references.

__This repo _presumes_ to find the minimal template that can be subsumed into ansible tasks lightly to generate yet complete vms.__


April 2025 wmartin

workAs this work is derived, informed by work of others, the most restrictive license found in that work, at ansible collections, is preserved.


## License

GNU General Public License v3.0 or later.
