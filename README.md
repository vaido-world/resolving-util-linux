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

### Before Reinstalling Utils-Linux

```
root@LiveCD ~]find / -name "libmount"
root@LiveCD ~]
```

```
root@LiveCD ~]find / -name "blkid"  
/Data/Variable/run/rootfsbase/Programs/Util-Linux/2.35.1/bin/blkid
/Data/Variable/run/rootfsbase/Programs/Util-Linux/2.35.1/share/bash-completion/completions/blkid
/Data/Variable/run/rootfsbase/System/Index/bin/blkid
/Data/Variable/run/rootfsbase/System/Index/share/bash-completion/completions/blkid
/Data/Variable/run/blkid
/Programs/Util-Linux/2.35.1/bin/blkid
/Programs/Util-Linux/2.35.1/share/bash-completion/completions/blkid
/System/Index/bin/blkid
/System/Index/share/bash-completion/completions/blkid
root@LiveCD ~]find / -name "catalog"

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



## Error in Thunar
```
Programs/Make/4.3/bin/make  all-recursive
make[1]: Entering directory '/Data/Compile/Sources/Thunar-1.8.9'
Making all in icons
make[2]: Entering directory '/Data/Compile/Sources/Thunar-1.8.9/icons'
Making all in 16x16
make[3]: Entering directory '/Data/Compile/Sources/Thunar-1.8.9/icons/16x16'
make[3]: Nothing to be done for 'all'.
make[3]: Leaving directory '/Data/Compile/Sources/Thunar-1.8.9/icons/16x16'
Making all in 24x24
make[3]: Entering directory '/Data/Compile/Sources/Thunar-1.8.9/icons/24x24'
make[3]: Nothing to be done for 'all'.
make[3]: Leaving directory '/Data/Compile/Sources/Thunar-1.8.9/icons/24x24'
Making all in 48x48
make[3]: Entering directory '/Data/Compile/Sources/Thunar-1.8.9/icons/48x48'
make[3]: Nothing to be done for 'all'.
make[3]: Leaving directory '/Data/Compile/Sources/Thunar-1.8.9/icons/48x48'
Making all in 64x64
make[3]: Entering directory '/Data/Compile/Sources/Thunar-1.8.9/icons/64x64'
make[3]: Nothing to be done for 'all'.
make[3]: Leaving directory '/Data/Compile/Sources/Thunar-1.8.9/icons/64x64'
Making all in 128x128
make[3]: Entering directory '/Data/Compile/Sources/Thunar-1.8.9/icons/128x128'
make[3]: Nothing to be done for 'all'.
make[3]: Leaving directory '/Data/Compile/Sources/Thunar-1.8.9/icons/128x128'
Making all in scalable
make[3]: Entering directory '/Data/Compile/Sources/Thunar-1.8.9/icons/scalable'
make[3]: Nothing to be done for 'all'.
make[3]: Leaving directory '/Data/Compile/Sources/Thunar-1.8.9/icons/scalable'
make[3]: Entering directory '/Data/Compile/Sources/Thunar-1.8.9/icons'
make[3]: Nothing to be done for 'all-am'.
make[3]: Leaving directory '/Data/Compile/Sources/Thunar-1.8.9/icons'
make[2]: Leaving directory '/Data/Compile/Sources/Thunar-1.8.9/icons'
Making all in pixmaps
make[2]: Entering directory '/Data/Compile/Sources/Thunar-1.8.9/pixmaps'
make[2]: Nothing to be done for 'all'.
make[2]: Leaving directory '/Data/Compile/Sources/Thunar-1.8.9/pixmaps'
Making all in po
make[2]: Entering directory '/Data/Compile/Sources/Thunar-1.8.9/po'
  MSGFMT am.gmo
  MSGFMT ar.gmo
  MSGFMT ast.gmo
  MSGFMT be.gmo
  MSGFMT bg.gmo
  MSGFMT bn.gmo
  MSGFMT ca.gmo
  MSGFMT cs.gmo
  MSGFMT da.gmo
  MSGFMT de.gmo
  MSGFMT el.gmo
  MSGFMT en_AU.gmo
  MSGFMT en_GB.gmo
  MSGFMT eo.gmo
  MSGFMT es.gmo
  MSGFMT et.gmo
  MSGFMT eu.gmo
  MSGFMT fa_IR.gmo
  MSGFMT fi.gmo
  MSGFMT fr.gmo
  MSGFMT gl.gmo
  MSGFMT he.gmo
  MSGFMT hr.gmo
  MSGFMT hu.gmo
  MSGFMT hy_AM.gmo
  MSGFMT hy.gmo
  MSGFMT id.gmo
  MSGFMT ie.gmo
  MSGFMT is.gmo
  MSGFMT it.gmo
  MSGFMT ja.gmo
  MSGFMT kk.gmo
  MSGFMT ko.gmo
  MSGFMT lt.gmo
  MSGFMT lv.gmo
  MSGFMT ms.gmo
  MSGFMT nb.gmo
  MSGFMT nl.gmo
  MSGFMT nn.gmo
  MSGFMT oc.gmo
  MSGFMT pa.gmo
  MSGFMT pl.gmo
  MSGFMT pt_BR.gmo
  MSGFMT pt.gmo
  MSGFMT ro.gmo
  MSGFMT ru.gmo
  MSGFMT si.gmo
  MSGFMT sk.gmo
  MSGFMT sl.gmo
  MSGFMT sq.gmo
  MSGFMT sr.gmo
  MSGFMT sv.gmo
  MSGFMT te.gmo
  MSGFMT th.gmo
  MSGFMT tr.gmo
  MSGFMT ug.gmo
  MSGFMT uk.gmo
  MSGFMT ur_PK.gmo
  MSGFMT ur.gmo
  MSGFMT vi.gmo
  MSGFMT zh_CN.gmo
  MSGFMT zh_HK.gmo
  MSGFMT zh_TW.gmo
make[2]: Leaving directory '/Data/Compile/Sources/Thunar-1.8.9/po'
Making all in thunarx
make[2]: Entering directory '/Data/Compile/Sources/Thunar-1.8.9/thunarx'
  CC       libthunarx_3_la-thunarx-config.lo
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
  CC       libthunarx_3_la-thunarx-file-info.lo
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
  CC       libthunarx_3_la-thunarx-menu.lo
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
  CC       libthunarx_3_la-thunarx-menu-item.lo
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
  CC       libthunarx_3_la-thunarx-menu-provider.lo
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
  CC       libthunarx_3_la-thunarx-preferences-provider.lo
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
  CC       libthunarx_3_la-thunarx-private.lo
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
  CC       libthunarx_3_la-thunarx-property-page.lo
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
  CC       libthunarx_3_la-thunarx-property-page-provider.lo
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
  CC       libthunarx_3_la-thunarx-provider-factory.lo
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
  CC       libthunarx_3_la-thunarx-provider-module.lo
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
  CC       libthunarx_3_la-thunarx-provider-plugin.lo
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
  CC       libthunarx_3_la-thunarx-renamer.lo
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
  CC       libthunarx_3_la-thunarx-renamer-provider.lo
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
  CCLD     libthunarx-3.la
  GISCAN   Thunarx-3.0.gir
cc1: warning: /System/Index/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /System/Index/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /System/Index/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /System/Index/include/blkid: No such file or directory [-Wmissing-include-dirs]
thunarx-private.h:36: Warning: Thunarx: symbol='I_': Unknown namespace for symbol 'I_'
  GICOMP   Thunarx-3.0.gir
make[2]: Leaving directory '/Data/Compile/Sources/Thunar-1.8.9/thunarx'
Making all in thunar
make[2]: Entering directory '/Data/Compile/Sources/Thunar-1.8.9/thunar'
/Programs/Make/4.3/bin/make  all-am
make[3]: Entering directory '/Data/Compile/Sources/Thunar-1.8.9/thunar'
  CC       thunar-thunar-marshal.o
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
  CC       thunar-thunar-dbus-freedesktop-interfaces.o
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
  CC       thunar-thunar-dbus-service-infos.o
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
  CC       thunar-thunar-thumbnailer-proxy.o
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
  CC       thunar-thunar-thumbnail-cache-proxy.o
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
  CC       thunar-thunar-resources.o
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/blkid: No such file or directory [-Wmissing-include-dirs]
cc1: warning: /usr/include/libmount: No such file or directory [-Wmissing-include-dirs]

```



## After reinstalling Util-Linux
```
root@LiveCD ~]find / -name "libmount"
/Data/Compile/Sources/util-linux-2.35.1/libmount
/Data/Compile/Sources/util-linux-2.35.1/tests/expected/libmount
/Data/Compile/Sources/util-linux-2.35.1/tests/ts/libmount
/Data/Variable/run/overlayfs/Programs/Util-Linux/2.35.1/include/libmount
/Data/Variable/run/overlayfs/Programs/Util-Linux/2.35.1/lib/python3.8/site-packages/libmount
/Data/Variable/run/overlayfs/System/Index/include/libmount
/Data/Variable/run/overlayfs/System/Index/lib/python3.8/site-packages/libmount
/Data/Variable/run/overlayfs/Data/Compile/Sources/util-linux-2.35.1/libmount
/Data/Variable/run/overlayfs/Data/Compile/Sources/util-linux-2.35.1/tests/expected/libmount
/Data/Variable/run/overlayfs/Data/Compile/Sources/util-linux-2.35.1/tests/ts/libmount
/Programs/Util-Linux/2.35.1/include/libmount
/Programs/Util-Linux/2.35.1/lib/python3.8/site-packages/libmount
/System/Index/include/libmount
/System/Index/lib/python3.8/site-packages/libmount

```

# libmount is part of util-linux
libmount is part of the util-linux package since version 2.18 and is available from
https://mirrors.edge.kernel.org/pub/linux/utils/util-linux/v2.18/
