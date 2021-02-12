vbox mac
=========

```

/usr/bin/VBoxManage modifyvm "catalina" --cpuidset 00000001 000106e5 00100800 0098e3fd bfebfbff

/usr/bin/VBoxManage setextradata "catalina" "VBoxInternal/Devices/efi/0/Config/DmiSystemProduct" "iMac11,3"

/usr/bin/VBoxManage setextradata "catalina" "VBoxInternal/Devices/efi/0/Config/DmiSystemVersion" "1.0"

/usr/bin/VBoxManage setextradata "catalina" "VBoxInternal/Devices/efi/0/Config/DmiBoardProduct" "Iloveapple"

/usr/bin/VBoxManage setextradata "catalina" "VBoxInternal/Devices/smc/0/Config/DeviceKey" "ourhardworkbythesewordsguardedpleasedontsteal(c)AppleComputerInc"

/usr/bin/VBoxManage setextradata "catalina" "VBoxInternal/Devices/smc/0/Config/GetKeyFromRealSMC" 1

/usr/bin/VBoxManage modifyvm "catalina" --cpu-profile "Intel Core i7-6700K"

/usr/bin/VBoxManage setextradata "catalina" VBoxInternal2/EfiGraphicsResolution 1680x1050

```
