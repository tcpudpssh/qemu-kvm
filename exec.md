sudo virt-install \
--name <vm> \
--memory 2048 \
--vcpus=2 --cpu \
host --cdrom /path/file.iso \
--disk pool=pool,\
size=20,\
bus=virtio,\
sparse=true,\
cache=none,\
io=native \
--network network=<net> \
--virt-type kvm \
--graphics=vnc
--print-xml
--noautoonsole