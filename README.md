# microraids
Fighting BITROT with every last breath

### Overview
I used to be a huge proponent of typical RAID. Back in the day of 2TB drives, disks were quite reliable. Even if a disk were to fail, I never had a problem doing a RAID recovery/resync onto a new disk. The RAID would keep running no problem even with 1 disk missing, up until the point a new disk could be inserted and replace the bad disk. From that perspective, the RAID system was very reliable. Fast-Forward to today where 8TB drives are ubiquitous and the chances of doing a RAID5 recovery on 9x8TB drives is 0.3%. I had to learn about bitrot the hard way, so here we are. The idea is that the fundamentals of RAID are still good, but doing a full recovery on a LARGE array in no longer a realistic option. (i.e. RAID5 on a 72TB array) I choose to make many small "microraids" to encapsulate my data. Each microraid is backed by a set of disk images, placed anywhere on any disk. For each microraid you can choose a different level of redundancy, even though they are stored on the same set of disks. microraids gives the flexibility to have any number of RAID 0/1/5/6 arrays as long as available drive space will allow it. Also each microraid can be checked for integrity and consistency in multiple ways.



### Supported OS
* [RapidLinux](https://github.com/Fullaxx/RapidLinux)
* [Slackware](http://www.slackware.com/)
* [Ubuntu Server 18.04](https://ubuntu.com/)

### Required Software
* [calc](https://sourceforge.net/projects/calc/) (Ubuntu: apt-get install apcalc)

### My Hardware Setup
* [Cooler Master Elite 110 RC-110-KKN2](https://www.amazon.com/dp/B00ID2FBU6)
* [ASRock J4105B-ITX](https://www.asrock.com/mb/Intel/J4105B-ITX/index.us.asp)
* [Ableconn PEX-SA130](https://www.amazon.com/dp/B07595M2MK) supports 2x Port Multiplier
* 2x [Mediasonic ProBox HF2-SU3S2](https://www.amazon.com/dp/B003X26VV4) connected via eSATA
* Initially I chose 8x [4TB HGST Ultrastar 7K4000 REFURB](https://www.amazon.com/dp/B0856WZT3B/) @ $60 each

### Alternate Hardware
* [SYBA SI-PEX40072](https://www.sybausa.com/index.php?route=product/product&product_id=155) also supports 2x Port Multiplier

### More Information
* [bitrot and atomic cows](https://arstechnica.com/information-technology/2014/01/bitrot-and-atomic-cows-inside-next-gen-filesystems/)
* [RAID questions](https://superuser.com/questions/1288587/btrfs-raid5-or-raid6-for-data-storage)
* [Raid Rebuild Probability Calc](http://www.raid-failure.com/raid5-failure.aspx)
* [URE in RAID](http://www.raidtips.com/raid5-ure.aspx)
