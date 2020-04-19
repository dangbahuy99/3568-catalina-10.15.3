

Open folder kext 

Right click AppleIntelWiFi.kext and click on Show Package Contents

Contents > info.plist

Open info.plist

Navigate to IOKitPersonalities > AppleIntelWiFi > NetWork Parameters > BSSID (your wifi name) > BSSID - 2 (leave blank) > PWD (password of the wifi you are connecting to in BSSID)
Save
 
cd ~/{you folder kext}
Open folder in Terminal and run :

sudo chown -R root:wheel AppleIntelWiFi.kext
sudo chmod -R 755 AppleIntelWiFi.kext
sudo kextload -v AppleIntelWiFi.kext/


Note: fix faild kextload
Terminal run :    sudo spctl --master-disable

Good luck :)
