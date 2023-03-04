Welcome,

This organization hosts the POC efforts for a [NVMe/TCP Boot-from-SAN](https://www.youtube.com/watch?v=1q89MqC1dZU) prototype that produces and consumes [ACPI](https://uefi.org/specifications) XSDT [NBFT](https://uefi.org/specs/ACPI/6.5/05_ACPI_Software_Programming_Model.html?highlight=nbft#description-header-signatures-for-tables-reserved-by-acpi) descriptors that are conformant to the [NVM Express Boot Specification 1.0](https://nvmexpress.org/specification/nvme-boot-specification/) and it’s interface with the [NVMe-oF messaging type](https://uefi.org/specs/UEFI/2.10/10_Protocols_Device_Path_Protocol.html#nvme-over-fabric-nvme-of-namespace-device-path) to [UEFI System Specification 2.10](https://uefi.org/specs/UEFI/2.10/).

Proof of Concept and Demonstrations:
* [suse-linux-poc](https://github.com/timberland-sig/suse-linux-poc) - Build your own openSUSE VM Boot-From SAN Envrionment.

Included repositories as part of this scope are:
* edk2 – With the timberland_1.0_final branch, which provides pre-OS driver support (Networking/NvmeOfDxe) which works with OVMF.
* spdk – Changes for edk2 support (as a submodule of edk2)
* libnvme – Library support for ACPI NBFT decoding from Linux userspace
* nvme-cli – Userspace command line to interact with and decode the ACPI NBFT
* dracut - Changes to dracut, a common Linux initram executable, for consuming the ACPI NBFT using nvme-cli.

Coming soon are instructions for setting up your Red Hat based POC environment too.
