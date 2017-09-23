# XPS-9560-Linux-WiFi-Intel-8265

I was able to make it work using:
```
options iwlwifi bt_coex_active=0
options iwlwifi swcrypto=1
options iwlwifi power_save=1
options iwlwifi 11n_disable=1
```

Personally, I think `11n_disable` has done the job.


Looks like this config works. Linux Mint 18.2 - *only when network usage is really low*.
```
➜  ~ uname -r
4.8.0-58-generic
➜  ~ dpkg -l linux-firmware
Wybór:U=nieznany/I=instalacja/R=usunięcie/P=wyczyszczenie/H=zatrzymanie
| Stan:N=brak/I=zainstalowany/C=skonfigurowany/U=rozpakowany/
|/  F=częśc. skonfigurowany/H=częśc. zainstalowany/W=wyzw. czek./T=wyzw. zapl.
|| Błędy?=(brak)/R-do pon. inst. (duże litery w "Stan" i "Błędy"=problemy)
||/ Nazwa          Wersja       Architektura Opis
+++-==============-============-============-=================================
ii  linux-firmware 1.164.1      all          Firmware for Linux kernel drivers
```
