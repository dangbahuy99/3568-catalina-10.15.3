Oh my friends who have met with the error failed to load - (libkern / kext) dependency load failed; check the system / kernel logs for errors or try kextutil (8) please try to replace the old IO80211Family.kext in your System/Library/Extension with the file(the same name) adove in this comment and reboot and then try again with what @skullpnuk have said:

Open Kext Updater
Tools
Rebuild Kextcache -> Start
Restart your system
Right click AppleIntelWiFi.kext and click on Show Package Contents
Contents > info.plist
Open info.plist
Navigate to IOKitPersonalities > AppleIntelWiFi > NetWork Parameters > BSSID (your wifi name) > BSSID - 2 (leave blank) > PWD (password of the wifi you are connecting to in BSSID)
Save
cd ~/Desktop

sudo chown -R root:wheel AppleIntelWiFi.kext
sudo chmod -R 755 AppleIntelWiFi.kext
sudo kextload -v AppleIntelWiFi.kext/


I have also met with the same error yesterday so I replaced the IO80211Family.kext and it works. You can find the reason of this solution in the previous comments under this issue on Feb 7 and Feb 8.

Have a try and good luck :)