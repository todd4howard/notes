vmware-toolbox-cmd disk shrink /

### 共享目录

```bash
vmware-hgfsclient

sudo vmhgfs-fuse .host:/ /mnt/hgfs -o subtype=vmhgfs-fuse,allow_other
```

```bash
ln -s /mnt/hgfs/Shared/Work ~/Work 
ln -s /mnt/hgfs/Shared/Study ~/Study
ln -s /mnt/hgfs/Shared/Tools ~/Tools
```
