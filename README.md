# Skeen's Virtual Gaming Rack Machine
Reference from the [Arch Linux wiki](https://wiki.archlinux.org/index.php/PCI_passthrough_via_OVMF/Examples#Skeen.27s_Virtual_Gaming_Rack_Machine)


Repository is layed out as `/` on the host.

Files:
* `etc/initramfs-tools/hooks/vfio-pci-override`: Adding the vfio-pci-override script and modules manually.
* `etc/initramfs-tools/modules`: Loading the vfio modules.
* `etc/libvirt/qemu/win10-2.xml`: LibVirt QEMU/KVM configuration file.
* `etc/modprobe.d/vfio.conf`: Installing the vfio-pci-override script.
* `home/skeen/Desktop/GF100.rom`: Original ROM pulled from ASUS GTX 480 using GPU-Z.
* `home/skeen/Desktop/GF100_updGOP.rom`: GOPupd'ated ROM referenced from the LibVirt configuration file.
* `usr/sbin/vfio-pci-override`: Script to support multiple identical GPUs.

Additionally, these files exist (not in `/`):
* `iommu-groups`: IOMMU groups found on the system (found using [this](https://wiki.archlinux.org/index.php/PCI_passthrough_via_OVMF#Ensuring_that_the_groups_are_valid)).
* `README.md`: The file you're reading right now.
* `vminfo`: Arch wiki text, with information about the setup.
