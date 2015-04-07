# start the installation
packer build -only=fedora-21-cloud-kvm fedora.json

# shrink the image size
qemu-img convert -c -f qcow2 -O qcow2 -o cluster_size=2M output-fedora-21-cloud-kvm/packer-fedora-21-cloud-kvm.qcow2 output-fedora-21-cloud-kvm/packer-fedora-21-cloud-kvm.compressed.qcow2

# upload the image to open stack
glance image-create --name "Fedora 21" --container-format ovf --disk-format qcow2 --file output-fedora-21-cloud-kvm/packer-fedora-21-cloud-kvm.compressed.qcow2 --is-public True --progress
