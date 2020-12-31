#Setup


dnf -y install haproxy httpd nfs-utils net-tools git wget ntp tree 


##selinux permissive
vi /etc/selinux/config
replace enforcing -> permissive

#HAProxy setup
cd  /etc/haproxy
cp -p /root/okd46-demo/haproxy/haproxy.cfg .


##Setup NFS
echo '/var/nfsshare 10.10.1.0/24(rw,sync,no_root_squash,no_all_squash,no_wdelay)' | sudo tee /etc/exports
###Test
exportfs

##Emable services
systemctl enable --now rpcbind nfs-server 
systemctl enable --now haproxy
systemctl enable --now httpd
