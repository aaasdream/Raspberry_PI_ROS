Tethered iPhone connection  
注意很多教學都沒有使用 usbmuxd 套件 導致失敗這裡加入安裝  
```
sudo apt-get -y install usbmuxd ipheth-utils libimobiledevice-utils ifuse
```
裝完之後  
```
ifconfig -s
```
應該會看到eth1 就是iphone上網了  
Iface      MTU    RX-OK RX-ERR RX-DRP RX-OVR    TX-OK TX-ERR TX-DRP TX-OVR Flg
eth0      1500        0      0      0 0             0      0      0      0 BMU
eth1      1500       12      0      1 0            14      0      0      0 BMRU
lo       65536       47      0      0 0            47      0      0      0 LRU
wlan0     1500    13721      0      0 0         10101      0      0      0 BMRU
