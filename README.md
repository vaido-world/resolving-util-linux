# resolving-util-linux

GoboLinux 017 Live CD seems to contain preinstalled Util-Linux 2.35.1

blkid command seems to be accessible from command line.

https://github.com/gobolinux/Recipes/blob/master/Util-Linux/2.35.1/Recipe#L16-L28

```
    # Fix broken links
    cd /Programs/Util-Linux/2.35.1/lib
    for i in \
    libblkid.so \
    libfdisk.so \
    libmount.so \
    libsmartcols.so \
    libuuid.so
    do
       # Point to the same target as ${i}.1
       ln -sf $(readlink ${i}.1) $i
    done
```

```
ls
addpart      fsck.minix   mkfs          swapoff
agetty       fsfreeze     mkfs.bfs      swapon
blkdiscard   fstrim       mkfs.cramfs   switch_root
blkid        getopt       mkfs.minix    taskset
blkzone      hardlink     mkswap        ul
blockdev     hexdump      more          umount
cal          hwclock      mount         uname26
cfdisk       i386         mountpoint    unshare
chcpu        ionice       namei         utmpdump
chfn         ipcmk        nologin       uuidd
chmem        ipcrm        nsenter       uuidgen
choom        ipcs         partx         uuidparse
chrt         isosize      pivot_root    wall
chsh         kill         prlimit       wdctl
col          last         raw           whereis
colcrt       lastb        readprofile   wipefs
colrm        ldattach     rename        write
column       linux32      renice        x86_64
ctrlaltdel   linux64      resizepart    XFCE4-Panel
delpart      logger       rev           XFCE4-Panel.tar.gz
dmesg        login        rfkill        XFCE4-Power-Manager
eject        look         rtcwake       XFCE4-Power-Manager.tar.gz
EXO          losetup      runuser       XFCE4-Session
EXO.tar.gz   lsblk        script        XFCE4-Session.tar.gz
fallocate    lscpu        scriptlive    XFCE4-Settings
fdformat     lsipc        scriptreplay  XFCE4-Settings.tar.gz
fdisk        lslocks      setarch       XFCE-Meta-Stable.tar.gz
fincore      lslogins     setsid        XFConf.tar.gz
findfs       lsmem        setterm       XFDesktop
findmnt      lsns         sfdisk        XFDesktop.tar.gz
flock        mcookie      su            XFWM4
fsck         mesg         sulogin       XFWM4.tar.gz
fsck.cramfs  Metare.bash  swaplabel     zramctl

```
