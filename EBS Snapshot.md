### EBS Snapshot = Point-in-time backup of an Amazon EBS volume.

### Can be used to:

- Restore volumes in case of failure.

- Create new volumes from snapshot.

- Migrate data across AZs or Regions.

### lab
- create a web-server 
- create a directory (myfolder) and file (myfile) with some text
- go to snapshots > create a snapshot > create
- snapshot > create a volume from snapshot > choose different AZ region > create volume 
- create another backup instance > choose instance (same as volume) > create
- volume > attach volume > choose backup instance > device name > done
- ec2-backup > connect > lsblk > mkdir /mnt/mybackup > run command: file -s /dev/nvme1n1 (creates a filesystem ) > mount -0 nouuid /dev/nvme1n1 /mnt/mybackup 
- cd /mnt/mybackup > cd home/myec2-user > cd myfolder/ > cat myfile

#### unmounnt 
- unmount -l /mnt/mybackup
- df -h

#### copy snapshot from one region to other
-  snapshot > actions > copy snapshot > different (target) region
- go to that target region now > snapshots > 
