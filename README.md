# Hacker-s-Flasdrive
In this I have Installed Kali Linux on Flasdrive and using some of the tools I have made the data to be stored on flashdrive persistent, 
which means that after performing any operation or after carrying task on Kali linux, data will be stored in the flashdrive itself and not  on the Computer,s RAM

###Technologies Reaquired:-Kali Linux, Flasdrive of min 8GB Storage, Disk image writer (eg Win32 Disk imager or Universal USB Installer) and MiniTool Partition Wizard.

Step 1: If you have torrent then search for Kali linux and install the disk image of Kali Linux, if mot then you first need to install torrent and then download the disk image of Kali Linux.You can use Universal USB Installer or Win32 Disk Imager but be sure that the flashdrive on which you will be writing the image must be formatted. Download and Insstall Universal USB Installer and follow given steps.
              Step a:- Select the Linux Distribution you want to install, in this case Kali Linux.
              Step b:- Browse the directory where you have saved the kali Linux Image and select the image file.
              Step c:- Select the Flashdrive on which you want to write the Image file.
              Step d:-Click 'Create' button in order to write the image file on the selected flashdrive.
Step 2:- Download and Install Minitool Partition Wizard and run this application. After running this applization, you will the storeage devices that are connected to the computer. You will see that there is still some space left in the flashdrive on which you have written the disk image. We can use the extra space in the flashdrive in order to make data persistent.For this you have to:-
              Step a: Right click on the drive on which Kali Linux is written and select Mover/Resize.
              Step b:- Drag the slinder to a decent amount until some few gray(extra) space.
              Step c:- Click 'Ok' Button. Right click on the 'Unallocated' space and select 'Create' and then click 'Yes'.
              Step d:- In the 'Partition Li' field type 'Persistence' without the single quotes. In the Create As field select the 
                        Primary option and in the File System select the Ext4 option. Click 'Ok' button.
              Step e:- Click the Apply button and then click Yes. After the partition is created click the Ok button.
Step 3:- Go to Start button on the Desktop, hold F2 and click Restart option
Step 4:- After this Computr will restart and there will be BIOS menue. You can navigate the the BIOS menu using the arrow keys.
Step 5:- Go to the Boot Tab. Click ont the 1st Boot and select flashdrive which has Kali Linux and then press ESC key.
Step 6:- After the loading Kali Linux GUI will appear on the monitor.Select the Kali Luux Persistane and enjoy the boot.
Step 7:- Once you have boosted into Kali Linux, we must now setup the persistence partition.To do this:-
              Step a:-Open Terminal and type the following command.
              1. #fdisk -l (its L not 1). It will display list of devices or partitions that are identified by Kali Linux.
                 the persistence partition is given by the name /dev/sdc2.
              2. #mkdir -p /mnt/UUI
              3. #mount /dev/sdc2 /mnt/UUI
              4. #echp " / union" >> /mnt/UUI/persistence.conf
              5. #umount /dev/sdc2 && reboot
              Step b:- Now press Enter and your computer will restart.
Step 8:- After you have rebboted your computer, you will see that the persistence icon must have disappeared from your desktop,
Which means you have Successfully created a Hacker's Flashdrive
              
