# nfs-client-provisioner

Provisioner that creates Persistent Volume automatically in the NFS server already configured through PersistentVolumeClaim.

## Dependencies

### nfs server

```bash
sudo apt update
sudo apt install nfs-kernel-server
echo '/srv/nfs/storage *(rw,sync,no_root_squash,insecure,no_subtree_check)' | sudo tee -a /etc/exports
sudo systemctl restart nfs-server
```
