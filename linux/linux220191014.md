### ifconfig

```
oot@kali:~# ifconfig
docker0: flags=4099<UP,BROADCAST,MULTICAST>  mtu 1500
        inet 172.17.0.1  netmask 255.255.0.0  broadcast 172.17.255.255
        ether 02:42:a0:1e:82:96  txqueuelen 0  (Ethernet)
        RX packets 0  bytes 0 (0.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 0  bytes 0 (0.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet6 fe80::a00:27ff:fe2a:d562  prefixlen 64  scopeid 0x20<link>
        ether 08:00:27:2a:d5:62  txqueuelen 1000  (Ethernet)
        RX packets 4  bytes 292 (292.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 31  bytes 4330 (4.2 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1000  (Local Loopback)
        RX packets 16  bytes 960 (960.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 16  bytes 960 (960.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

```
```
有3個介面(interfaces):
[1]docker 0
[2]eth0 實體網卡
[3]lo==loaclhost每一台電曩都會有本地端位址  127.0.0.1
```

```
解釋下列資訊的意義:
mtu 1500
inet 172.17.0.1  
netmask 255.255.0.0  
broadcast 172.17.255.255
ether 02:42:a0:1e:82:96
```
```
問題1.IP位址==?  
問題2.mtu 1500  最大傳輸單元Maximum Transmission Unit  https://en.wikipedia.org/wiki/Maximum_transmission_unit
問題3.MAC address==實體網卡位址==>ether 08:00:27:2a:d5:62
問題4.broadcast address==https://en.wikipedia.org/wiki/Broadcast_address
問題5.lo==localhost address=?
```
# ping 172.17.0.1

```

```

### linux實戰作業.md
```
root@kali:~# pwd
/root
root@kali:~# cd ..
root@kali:/# pwd
/
```
# linux pwd 
```
https://hungwei0331.pixnet.net/blog/post/352643434-linux---pwd%E6%8C%87%E4%BB%A4
pwd為print name of current/working directory的縮寫

顧名思義pwd用於顯示目前所在目錄的指令,
想要知道目前所在的目錄，可以輸入pwd即可：
1. 列出目前的工作目錄:
#pwd

2. 顯示出實際的工作目錄，而非連結檔本身的目錄名
#pwd -P

3. 目錄連接鏈結時，輸出連接路徑
#pwd -L

bin==binary 執行檔

root@kali:/# cd bin
root@kali:/bin# pwd -L
/bin
root@kali:/bin# pwd -P
/usr/bin

回到上層目錄===>cd ..
```
### 測驗:說明底下程式的意義
```
root@kali:/bin# cd ..
root@kali:/# cd
root@kali:~# 
```
```
root@kali:/# ls
0     etc             lib     lost+found  proc  srv  var
bin   home            lib32   media       root  sys  vmlinuz
boot  initrd.img      lib64   mnt         run   tmp  vmlinuz.old
dev   initrd.img.old  libx32  opt         sbin  usr
```

### 作業一:說明linux 上述的目錄結構

