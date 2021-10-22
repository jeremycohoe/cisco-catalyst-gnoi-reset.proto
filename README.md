# Cisco Catalyst gNOI reset.proto

# Running gnoi_reset

```
auto@pod24-xelab:~$ ./gnoi_reset -target_addr 10.1.1.5:50052 -target_name dd -notls -zero_fill
I1014 11:53:15.248633 2761247 gnoi_reset.go:59] Reset Called Successfully!
auto@pod24-xelab:~$
```

# Console log

```
C9300#
Chassis 1 reloading, reason - Factory Reset
Oct 14 11:50:31.175: %PMAN-5-EXITACTION: F0/0: pvp: Process manager is exiting: reload fp action requested
Oct 14 11:50:32.839: %PMAN-5-EXITACTION: R0/0: pvp: Pger is exiting: rp processes exit with reload switch code


Enabling factory reset for this reload cycle
 Switch booted with flash:packages.conf
 Switch booted via packages.conf
FACTORY-RESET-RESTORE-IMAGE Taking backup of flash:packages.conf
FACTORY-RESET-RESTORE-IMAGE Searching for packages.conf on flash
factory-reset-restore-image taking a backup of packages.conf from flash
factory-reset-restore-image copying cat9k-cc_srdriver.BLD_V177_THROTTLE_LATEST_20210929_030812_V17_7_0_106_2.SSA.pkg to /tmp/factory_reset
factory-reset-restore-image copying cat9k-espbase.BLD_V177_THROTTLE_LATEST_20210929_030812_V17_7_0_106_2.SSA.pkg to /tmp/factory_reset
factory-reset-restore-image copying cat9k-guestshell.BLD_V177_THROTTLE_LATEST_20210929_030812_V17_7_0_106_2.SSA.pkg to /tmp/factory_reset
factory-reset-restore-image copying cat9k-rpbase.BLD_V177_THROTTLE_LATEST_20210929_030812_V17_7_0_106_2.SSA.pkg to /tmp/factory_reset
factory-reset-restore-image copying cat9k-sipbase.BLD_V177_THROTTLE_LATEST_20210929_030812_V17_7_0_106_2.SSA.pkg to /tmp/factory_reset
factory-reset-restore-image copying cat9k-sipspa.BLD_V177_THROTTLE_LATEST_20210929_030812_V17_7_0_106_2.SSA.pkg to /tmp/factory_reset
factory-reset-restore-image copying cat9k-srdriver.BLD_V177_THROTTLE_LATEST_20210929_030812_V17_7_0_106_2.SSA.pkg to /tmp/factory_reset
factory-reset-restore-image copying cat9k-webui.BLD_V177_THROTTLE_LATEST_20210929_030812_V17_7_0_106_2.SSA.pkg to /tmp/factory_reset
factory-reset-restore-image copying cat9k-wlc.BLD_V177_THROTTLE_LATEST_20210929_030812_V17_7_0_106_2.SSA.pkg to /tmp/factory_reset
factory-reset-restore-image copying cat9k-rpboot.BLD_V177_THROTTLE_LATEST_20210929_030812_V17_7_0_106_2.SSA.pkg to /tmp/factory_reset
factory-reset-restore-image copying packages.conf to /tmp/factory_reset
% FACTORYRESET - Started Cleaning Up...

% FACTORYRESET - Unmounting sd1
% FACTORYRESET - Cleaning Up sd1 [0]
% FACTORYRESET - erase In progress.. please wait for completion...
% FACTORYRESET - write zero...
% FACTORYRESET - finish erase

% FACTORYRESET - Making File System sd1 [0]
Creating filesystem with 409600 4k blocks and 102544 inodes
Filesystem UUID: fd34e17f-1407-44bc-a859-14832be035ee
Superblock backups stored on blocks:
        32768, 98304, 163840, 229376, 294912

Allocating group tables: done
Writing inode tables: done
Writing superblocks and filesystem accounting information: done

% FACTORYRESET - Mounting Back sd1 [0]
% FACTORYRESET - Handling Mounted sd1
% FACTORYRESET - Factory Reset Done for sd1

% FACTORYRESET - Unmounting sd3
% FACTORYRESET - Cleaning Up sd3 [0]
% FACTORYRESET - erase In progress.. please wait for completion...
% FACTORYRESET - write zero...
% FACTORYRESET - finish erase

% FACTORYRESET - Making File System sd3 [0]
Creating filesystem with 2816000 4k blocks and 704512 inodes
Filesystem UUID: 50e430a9-ff1f-4bc7-83dd-a565d1ca887b
Superblock backups stored on blocks:
        32768, 98304, 163840, 229376, 294912, 819200, 884736, 1605632, 2654208

Allocating group tables: done
Writing inode tables: done
Writing superblocks and filesystem accounting information: done

% FACTORYRESET - Mounting Back sd3 [0]
% FACTORYRESET - Handling Mounted sd3
% FACTORYRESET - Factory Reset Done for sd3

% FACTORYRESET - Unmounting sd6
% FACTORYRESET - Cleaning Up sd6 [0]
% FACTORYRESET - erase In progress.. please wait for completion...
% FACTORYRESET - write zero...
% FACTORYRESET - finish erase

% FACTORYRESET - Making File System sd6 [0]
Creating filesystem with 131072 1k blocks and 32768 inodes
Filesystem UUID: 322856ea-75e2-437f-ad60-e39ebb1b8fa6
Superblock backups stored on blocks:
        8193, 24577, 40961, 57345, 73729

Allocating group tables: done
Writing inode tables: done
Writing superblocks and filesystem accounting information: done

% FACTORYRESET - Mounting Back sd6 [0]
% FACTORYRESET - Handling Mounted sd6
% FACTORYRESET - Factory Reset Done for sd6
% FACTORYRESET - Lic Clean UP
% FACTORYRESET - Lic Clean Successful...
% FACTORYRESET - Clean Up Successful...
% FACTORYRESET - Check if usbflash0 is mounted...
% FACTORYRESET - Check if usbflash1 is mounted...
% FACTORYRESET - usbflash1 detected..
% FACTORYRESET - Proceed with Unmounting the USB3.0 SSD...
% FACTORYRESET - Cleaning Up /vol/usb1
% FACTORYRESET - In progress.. please wait for completion...
% FACTORYRESET - Making File System on SSD
Discarding device blocks: done
Creating filesystem with 29304945 4k blocks and 7331840 inodes
Filesystem UUID: 4d1427ce-70eb-4323-b1b3-ee16a17205e8
Superblock backups stored on blocks:
        32768, 98304, 163840, 229376, 294912, 819200, 884736, 1605632, 2654208,
        4096000, 7962624, 11239424, 20480000, 23887872

Allocating group tables: done
Writing inode tables: done
Creating journal (32768 blocks): done
Writing superblocks and filesystem accounting information: done

% FACTORYRESET - Mounting Back usbflash1
% FACTORYRESET - Factory reset done for SSD
FACTORY-RESET-RESTORE-IMAGE Copying back image from /tmp/factory_reset onto /bootflash
ReloadReason=Factory Reset
FACTORY-RESET-RESTORE-IMAGE Factory reset successful. Continuing with reboot...
Setting BOOT image
Factory reset successful. Rebooting...

Initializing Hardware......

System Bootstrap, Version 17.6.1r[FC2], RELEASE SOFTWARE (P)
Compiled Wed 05/12/2021 15:39:34.01 by rel

Current ROMMON image : Primary
Last reset cause     : SoftwareReload
C9300-24P platform with 8388608 Kbytes of main memory

boot: attempting to boot from [flash:packages.conf]
boot: reading file packages.conf
#
#######################################################################################################################################################################################################################################################################################################################################################################################################################################################################################################################################


Both links down, not waiting for other switches
Switch number is 1

              Restricted Rights Legend

Use, duplication, or disclosure by the Government is
subject to restrictions as set forth in subparagraph
(c) of the Commercial Computer Software - Restricted
Rights clause at FAR sec. 52.227-19 and subparagraph
(c) (1) (ii) of the Rights in Technical Data and Computer
Software clause at DFARS sec. 252.227-7013.

           Cisco Systems, Inc.
           170 West Tasman Drive
           San Jose, California 95134-1706



Cisco IOS Software [Cupertino], Catalyst L3 Switch Software (CAT9K_IOSXE), Experimental Version 17.7.20210929:032559 [S2C-build-v177_throttle-1063-/nobackup/mcpre/BLD-BLD_V177_THROTTLE_LATEST_20210929_030812 133]
Copyright (c) 1986-2021 by Cisco Systems, Inc.
Compiled Wed 29-Sep-21 10:26 by mcpre


This software version supports only Smart Licensing as the software licensing mechanism.


PLEASE READ THE FOLLOWING TERMS CAREFULLY. INSTALLING THE LICENSE OR
LICENSE KEY PROVIDED FOR ANY CISCO SOFTWARE PRODUCT, PRODUCT FEATURE,
AND/OR SUBSEQUENTLY PROVIDED SOFTWARE FEATURES (COLLECTIVELY, THE
"SOFTWARE"), AND/OR USING SUCH SOFTWARE CONSTITUTES YOUR FULL
ACCEPTANCE OF THE FOLLOWING TERMS. YOU MUST NOT PROCEED FURTHER IF YOU
ARE NOT WILLING TO BE BOUND BY ALL THE TERMS SET FORTH HEREIN.

Your use of the Software is subject to the Cisco End User License Agreement
(EULA) and any relevant supplemental terms (SEULA) found at
http://www.cisco.com/c/en/us/about/legal/cloud-and-software/software-terms.html.

You hereby acknowledge and agree that certain Software and/or features are
licensed for a particular term, that the license to such Software and/or
features is valid only for the applicable term and that such Software and/or
features may be shut down or otherwise terminated by Cisco after expiration
of the applicable license term (e.g., 90-day trial period). Cisco reserves
the right to terminate any such Software feature electronically or by any
other means available. While Cisco may provide alerts, it is your sole
responsibility to monitor your usage of any such term Software feature to
ensure that your systems and networks are prepared for a shutdown of the
Software feature.


% Checking backup nvram
% No config present. Using default config

FIPS: Flash Key Check : Key Not Found, FIPS Mode Not Enabled
cisco C9300-24P (X86) processor with 1319374K/6147K bytes of memory.
Processor board ID FCW2241DHBN
2048K bytes of non-volatile configuration memory.
8388608K bytes of physical memory.
1638400K bytes of Crash Files at crashinfo:.
11264000K bytes of Flash at flash:.

Base Ethernet MAC Address          : 70:35:09:9e:b9:80
Motherboard Assembly Number        : 73-18271-03
Motherboard Serial Number          : FOC22396PK1
Model Revision Number              : A0
Motherboard Revision Number        : A0
Model Number                       : C9300-24P
System Serial Number               : FCW2241DHBN
CLEI Code Number                   :


No startup-config, starting autoinstall/pnp/ztp...

Autoinstall will terminate if any input is detected on console


```

# End
