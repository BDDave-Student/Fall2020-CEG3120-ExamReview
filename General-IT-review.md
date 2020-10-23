## IT Knowledge

- Partition tables, partitions, filesystems
- Mounting partition(s)
  - Role of /etc/fstab:  File Systems Table configurations file.  Contains information on mounted devices and what they individually do (mounted partition OS, data storage,
  - Partition requires:  Partition Table, Partition, File System, Mounting Point
- RAID 0, 1, 5, 6
  - Given situation, which RAID would you recommend?
    * The higher the raid, the more resistant to faulting data the database can tolerate
    * Raid 0:  Introduction of Striping = split data across blocks; Introduction of performance increase in read/write. 
    * Raid 1:  Introduction of Mirroring = evolved striping across 2 blocks, evolved faster performance of read and write, fault tolerant
    * Raid 5 single parity (1 block works in place of 1 other block that has failed)  Raid 6 double parity
- cronjobs:  Time based scheduler to automate tasks given a specified time/period - * minutes, * hours, * day of month, * month, * day of the week
  - Where to add a cronjob - cat /tmp/crontab
  - Format of a cronjob - * * * * * \[script path]
