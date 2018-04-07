# Python Scripting 

### The vbr.py is a simple Python script that will attempt to read the volume boot record (VBR) from an image file. The  volume boot record (VBR) is also known as a volume boot sector.


### The mbr.py is a simple Python script that will attempt to mount partitions from an image file. Images are mounted in read-only mode.



### ls -lh
total 77G  
-rw-r--r--. 1 akmtir akmtir 469M Apr  6 21:49 Fat16.dd  
-rw-r--r--. 1 root   root   1.9G Apr  7 10:37 Fat32.dd  
-rw-r--r--. 1 root   root    75G Apr  7 13:14 HD_NTFS.dd  
-rw-rw-r--. 1 akmtir akmtir 5.9K Apr  7 14:18 mbr.py  
-rw-rw-r--. 1 akmtir akmtir 8.1K Apr  7 14:18 vbr.py  


### sudo python3 vbr.py Fat16.dd
Looks like a MBR or VBR  
MBR signature valid: True  
Partition 1 information:  
	Bootable: True  
	Start head: 15  
	Start sector: 10  
	Start cylinder: 0  
	Partition type: 6  
	End head: 31  
	End sector: 32  
	End cylinder: 171  
	Reserved sectors: 489  
	Total sectors: 958999  
Partition 2 information:  
	Entry is empty.  
Partition 3 information:  
	Entry is empty.  
Partition 4 information:  
	Entry is empty.  
Found Volume with type b'FAT16   '  
Volume label: b'PHONE CARD '  
Total sectors: 949408  
Cluster 14: 917  
Sector: 14  


### sudo python3 vbr.py Fat32.dd 
Looks like a MBR or VBR  
MBR signature valid: True  
Partition 1 information:  
	Bootable: True  
	Start head: 32  
	Start sector: 33  
	Start cylinder: 0  
	Partition type: 12  
	End head: 254  
	End sector: 63  
	End cylinder: 242  
	Reserved sectors: 2048  
	Total sectors: 3903360  
Partition 2 information:  
	Entry is empty.  
Partition 3 information:  
	Entry is empty.  
Partition 4 information:  
	Entry is empty.  
Found Volume with type b'FAT32   '  
Volume label: b'NO NAME    '  
Total sectors: 3903360  
Cluster 14: 8288  
Sector: 14  


### sudo python3 vbr.py HD_NTFS.dd 
Looks like a MBR or VBR  
MBR signature valid: True  
Partition 1 information:  
	Bootable: True  
	Start head: 32  
	Start sector: 33  
	Start cylinder: 0  
	Partition type: 135  
	End head: 83  
	End sector: 62  
	End cylinder: 129  
	Reserved sectors: 2048  
	Total sectors: 39073323  
Partition 2 information:  
	Bootable: False  
	Start head: 91  
	Start sector: 28  
	Start cylinder: 129  
	Partition type: 135  
	End head: 26  
	End sector: 62  
	End cylinder: 171  
	Reserved sectors: 39075840  
	Total sectors: 13024655  
Partition 3 information:  
	Bootable: False  
	Start head: 36  
	Start sector: 58  
	Start cylinder: 171  
	Partition type: 135  
	End head: 167  
	End sector: 62  
	End cylinder: 3  
	Reserved sectors: 52101120  
	Total sectors: 26049623  
Partition 4 information:  
	Bootable: False  
	Start head: 182  
	Start sector: 55  
	Start cylinder: 3  
	Partition type: 5  
	End head: 80  
	End sector: 63  
	End cylinder: 3  
	Reserved sectors: 78151680  
	Total sectors: 78149808  
Found Volume with type b'\x00\x00\xfa3\xc0\x8e\xd0\xbc'  
Volume label: b'\x00\xdf\x81\xc3\xd0\xc5\xc3\xd0\xbe\x00\x00'  
Total sectors: 0  
Cluster 14: 96  
Sector: 14  
Sorry GPT and extended partitions are not supported by this script!  


### sudo python3 mbr.py HD_NTFS.dd 
Looks like a MBR or VBR  
MBR signature valid: True  
Partition 1 information:  
	Bootable: True  
	Start head: 32  
	Start sector: 33  
	Start cylinder: 0  
	Partition type: 135  
	End head: 83  
	End sector: 62  
	End cylinder: 129  
	Reserved sectors: 2048  
	Total sectors: 39073323  
Partition 2 information:  
	Bootable: False  
	Start head: 91  
	Start sector: 28  
	Start cylinder: 129  
	Partition type: 135  
	End head: 26  
	End sector: 62  
	End cylinder: 171  
	Reserved sectors: 39075840  
	Total sectors: 13024655  
Partition 3 information:  
	Bootable: False  
	Start head: 36  
	Start sector: 58  

...  


[Ak. MT. 01-04-2018](http://www.akmtir.com/)

