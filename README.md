# Python Scripting 

### The vbr.py is a simple Python script that will attempt to read the volume boot record (VBR) from an image file. The  volume boot record (VBR) is also known as a volume boot sector.


### The mbr.py is a simple Python script that will attempt to mount partitions from an image file. Images are mounted in read-only mode.



**_ls -lh_**  
total 77G  
-rw-r--r--. 1 akmtir akmtir 469M Apr  6 21:49 Fat16.dd  
-rw-r--r--. 1 root   root   1.9G Apr  7 10:37 Fat32.dd  
-rw-r--r--. 1 root   root    75G Apr  7 13:14 HD_NTFS.dd  
-rw-rw-r--. 1 akmtir akmtir 5.9K Apr  7 14:18 mbr.py  
-rw-rw-r--. 1 akmtir akmtir 8.1K Apr  7 14:18 vbr.py  


**_sudo python3 vbr.py Fat16.dd_**  
Looks like a MBR or VBR  
MBR signature valid: True  
Partition 1 information:  
&nbsp;&nbsp;&nbsp;&nbsp;   Bootable: True  
&nbsp;&nbsp;&nbsp;&nbsp;   Start head: 15  
&nbsp;&nbsp;&nbsp;&nbsp;   Start sector: 10  
&nbsp;&nbsp;&nbsp;&nbsp;   Start cylinder: 0  
&nbsp;&nbsp;&nbsp;&nbsp;   Partition type: 6  
&nbsp;&nbsp;&nbsp;&nbsp;   End head: 31  
&nbsp;&nbsp;&nbsp;&nbsp;   End sector: 32  
&nbsp;&nbsp;&nbsp;&nbsp;   End cylinder: 171  
&nbsp;&nbsp;&nbsp;&nbsp;   Reserved sectors: 489  
&nbsp;&nbsp;&nbsp;&nbsp;   Total sectors: 958999  
Partition 2 information:  
&nbsp;&nbsp;&nbsp;&nbsp;   Entry is empty.  
Partition 3 information:  
&nbsp;&nbsp;&nbsp;&nbsp;   Entry is empty.  
Partition 4 information:  
&nbsp;&nbsp;&nbsp;&nbsp;   Entry is empty.  
Found Volume with type b'FAT16   '  
Volume label: b'PHONE CARD '  
Total sectors: 949408  
Cluster 14: 917  
Sector: 14  


**_sudo python3 vbr.py Fat32.dd_**  
Looks like a MBR or VBR  
MBR signature valid: True  
Partition 1 information:  
&nbsp;&nbsp;&nbsp;&nbsp;   Bootable: True  
&nbsp;&nbsp;&nbsp;&nbsp;   Start head: 32  
&nbsp;&nbsp;&nbsp;&nbsp;   Start sector: 33  
&nbsp;&nbsp;&nbsp;&nbsp;   Start cylinder: 0  
&nbsp;&nbsp;&nbsp;&nbsp;   Partition type: 12  
&nbsp;&nbsp;&nbsp;&nbsp;   End head: 254  
&nbsp;&nbsp;&nbsp;&nbsp;   End sector: 63  
&nbsp;&nbsp;&nbsp;&nbsp;   End cylinder: 242  
&nbsp;&nbsp;&nbsp;&nbsp;   Reserved sectors: 2048  
&nbsp;&nbsp;&nbsp;&nbsp;   Total sectors: 3903360  
Partition 2 information:  
&nbsp;&nbsp;&nbsp;&nbsp;   Entry is empty.  
Partition 3 information:  
&nbsp;&nbsp;&nbsp;&nbsp;   Entry is empty.  
Partition 4 information:  
&nbsp;&nbsp;&nbsp;&nbsp;   Entry is empty.  
Found Volume with type b'FAT32   '  
Volume label: b'NO NAME    '  
Total sectors: 3903360  
Cluster 14: 8288  
Sector: 14  


**_sudo python3 vbr.py HD_NTFS.dd_**  
Looks like a MBR or VBR  
MBR signature valid: True  
Partition 1 information:  
&nbsp;&nbsp;&nbsp;&nbsp;   Bootable: True  
&nbsp;&nbsp;&nbsp;&nbsp;   Start head: 32  
&nbsp;&nbsp;&nbsp;&nbsp;   Start sector: 33  
&nbsp;&nbsp;&nbsp;&nbsp;   Start cylinder: 0  
&nbsp;&nbsp;&nbsp;&nbsp;   Partition type: 135  
&nbsp;&nbsp;&nbsp;&nbsp;   End head: 83  
&nbsp;&nbsp;&nbsp;&nbsp;   End sector: 62  
&nbsp;&nbsp;&nbsp;&nbsp;   End cylinder: 129  
&nbsp;&nbsp;&nbsp;&nbsp;   Reserved sectors: 2048  
&nbsp;&nbsp;&nbsp;&nbsp;   Total sectors: 39073323  
Partition 2 information:  
&nbsp;&nbsp;&nbsp;&nbsp;   Bootable: False  
&nbsp;&nbsp;&nbsp;&nbsp;   Start head: 91  
&nbsp;&nbsp;&nbsp;&nbsp;   Start sector: 28  
&nbsp;&nbsp;&nbsp;&nbsp;   Start cylinder: 129  
&nbsp;&nbsp;&nbsp;&nbsp;   Partition type: 135  
&nbsp;&nbsp;&nbsp;&nbsp;   End head: 26  
&nbsp;&nbsp;&nbsp;&nbsp;   End sector: 62  
&nbsp;&nbsp;&nbsp;&nbsp;   End cylinder: 171  
&nbsp;&nbsp;&nbsp;&nbsp;   Reserved sectors: 39075840  
&nbsp;&nbsp;&nbsp;&nbsp;   Total sectors: 13024655  
Partition 3 information:  
&nbsp;&nbsp;&nbsp;&nbsp;   Bootable: False  
&nbsp;&nbsp;&nbsp;&nbsp;   Start head: 36  
&nbsp;&nbsp;&nbsp;&nbsp;   Start sector: 58  
&nbsp;&nbsp;&nbsp;&nbsp;   Start cylinder: 171  
&nbsp;&nbsp;&nbsp;&nbsp;   Partition type: 135  
&nbsp;&nbsp;&nbsp;&nbsp;   End head: 167  
&nbsp;&nbsp;&nbsp;&nbsp;   End sector: 62  
&nbsp;&nbsp;&nbsp;&nbsp;   End cylinder: 3  
&nbsp;&nbsp;&nbsp;&nbsp;   Reserved sectors: 52101120  
&nbsp;&nbsp;&nbsp;&nbsp;   Total sectors: 26049623  
Partition 4 information:  
&nbsp;&nbsp;&nbsp;&nbsp;   Bootable: False  
&nbsp;&nbsp;&nbsp;&nbsp;   Start head: 182  
&nbsp;&nbsp;&nbsp;&nbsp;   Start sector: 55  
&nbsp;&nbsp;&nbsp;&nbsp;   Start cylinder: 3  
&nbsp;&nbsp;&nbsp;&nbsp;   Partition type: 5  
&nbsp;&nbsp;&nbsp;&nbsp;   End head: 80  
&nbsp;&nbsp;&nbsp;&nbsp;   End sector: 63  
&nbsp;&nbsp;&nbsp;&nbsp;   End cylinder: 3  
&nbsp;&nbsp;&nbsp;&nbsp;   Reserved sectors: 78151680  
&nbsp;&nbsp;&nbsp;&nbsp;   Total sectors: 78149808  
Found Volume with type b'\x00\x00\xfa3\xc0\x8e\xd0\xbc'  
Volume label: b'\x00\xdf\x81\xc3\xd0\xc5\xc3\xd0\xbe\x00\x00'  
Total sectors: 0  
Cluster 14: 96  
Sector: 14  
Sorry GPT and extended partitions are not supported by this script!  


**_sudo python3 mbr.py HD_NTFS.dd_**  
Looks like a MBR or VBR  
MBR signature valid: True  
Partition 1 information:  
&nbsp;&nbsp;&nbsp;&nbsp;   Bootable: True  
&nbsp;&nbsp;&nbsp;&nbsp;   Start head: 32  
&nbsp;&nbsp;&nbsp;&nbsp;   Start sector: 33  
&nbsp;&nbsp;&nbsp;&nbsp;   Start cylinder: 0  
&nbsp;&nbsp;&nbsp;&nbsp;   Partition type: 135  
&nbsp;&nbsp;&nbsp;&nbsp;   End head: 83  
&nbsp;&nbsp;&nbsp;&nbsp;   End sector: 62  
&nbsp;&nbsp;&nbsp;&nbsp;   End cylinder: 129  
&nbsp;&nbsp;&nbsp;&nbsp;   Reserved sectors: 2048  
&nbsp;&nbsp;&nbsp;&nbsp;   Total sectors: 39073323  
Partition 2 information:  
&nbsp;&nbsp;&nbsp;&nbsp;   Bootable: False  
&nbsp;&nbsp;&nbsp;&nbsp;   Start head: 91  
&nbsp;&nbsp;&nbsp;&nbsp;   Start sector: 28  
&nbsp;&nbsp;&nbsp;&nbsp;   Start cylinder: 129  
&nbsp;&nbsp;&nbsp;&nbsp;   Partition type: 135  
&nbsp;&nbsp;&nbsp;&nbsp;   End head: 26  
&nbsp;&nbsp;&nbsp;&nbsp;   End sector: 62  
&nbsp;&nbsp;&nbsp;&nbsp;   End cylinder: 171  
&nbsp;&nbsp;&nbsp;&nbsp;   Reserved sectors: 39075840  
&nbsp;&nbsp;&nbsp;&nbsp;   Total sectors: 13024655  
Partition 3 information:  
&nbsp;&nbsp;&nbsp;&nbsp;   Bootable: False  
&nbsp;&nbsp;&nbsp;&nbsp;   Start head: 36  
&nbsp;&nbsp;&nbsp;&nbsp;   Start sector: 58  

...  


[Ak. MT. 07-04-2018](http://www.akmtir.com/)

