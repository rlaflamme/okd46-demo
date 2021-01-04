#Setup

qm stop 300 && qm destroy 300
qm create 300 --pool gokd-46 --memory 8192 --cores 4 --scsi0 local-zfs:120 --ide2 local:iso/fedora-coreos-32.20201104.3.0-live.x86_64.iso,media=cdrom,size=744M --name okd4-bootstrap --net0 virtio=6a:7b:d0:7f:5f:e0,bridge=vmbr3 --numa 0 --scsihw virtio-scsi-pci --ostype l26 --onboot no --sockets 1
qm stop 301 && qm destroy 301
qm create 301 --pool gokd-46 --memory 16384 --cores 4 --scsi0 local-zfs:120 --ide2 local:iso/fedora-coreos-32.20201104.3.0-live.x86_64.iso,media=cdrom,size=744M --name okd4-control-plane-1 --net0 virtio=76:c4:8d:d2:1c:4b,bridge=vmbr3 --numa 0 --scsihw virtio-scsi-pci --ostype l26 --onboot no --sockets 1
qm stop 302 && qm destroy 302
qm create 302 --pool gokd-46 --memory 16384 --cores 4 --scsi0 local-zfs:120 --ide2 local:iso/fedora-coreos-32.20201104.3.0-live.x86_64.iso,media=cdrom,size=744M --name okd4-control-plane-2 --net0 virtio=22:2f:f7:24:d5:f6,bridge=vmbr3 --numa 0 --scsihw virtio-scsi-pci --ostype l26 --onboot no --sockets 1
qm stop 303 && qm destroy 303
qm create 303 --pool gokd-46 --memory 16384 --cores 4 --scsi0 local-zfs:120 --ide2 local:iso/fedora-coreos-32.20201104.3.0-live.x86_64.iso,media=cdrom,size=744M --name okd4-control-plane-3 --net0 virtio=ce:c2:9d:a6:6d:f2,bridge=vmbr3 --numa 0 --scsihw virtio-scsi-pci --ostype l26 --onboot no --sockets 1
qm stop 304 && qm destroy 304
qm create 304 --pool gokd-46 --memory 16384 --cores 4 --scsi0 local-zfs:120 --ide2 local:iso/fedora-coreos-32.20201104.3.0-live.x86_64.iso,media=cdrom,size=744M --name okd4-compute-1 --net0 virtio=a2:ea:17:4c:80:11,bridge=vmbr3 --numa 0 --scsihw virtio-scsi-pci --ostype l26 --onboot no --sockets 1
qm stop 305 && qm destroy 305
qm create 305 --pool gokd-46 --memory 16384 --cores 4 --scsi0 local-zfs:120 --ide2 local:iso/fedora-coreos-32.20201104.3.0-live.x86_64.iso,media=cdrom,size=744M --name okd4-compute-2 --net0 virtio=c2:5f:7e:9d:e9:b9,bridge=vmbr3 --numa 0 --scsihw virtio-scsi-pci --ostype l26 --onboot no --sockets 1

