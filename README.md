# ROCKPro64 Fan Controller
This system is a Python-based service for controlling the fan connected to the PWM FAN connector on the ROCKPro64 SMB. The fan speed is configurable as a text
file to optimize for thermals or noise.

# Installing
Installing can be done with the following:
```
git clone https://github.com/Taurolyon/ROCKPro64-Fan-Controller.git
```
```
cd ROCKPro64-Fan-Controller
```
```
sudo chmod +x ./*.sh
```
```
sudo ./Installer.sh
```

# Uninstalling
Uninstalling can be done with the following:
```
sudo ./Uninstaller.sh
```

# Customizing The Fan Curve
By default, the fan curve file is in `/etc/FanControl/FanCurve.txt`. Each line
contains a fan curve point, with the first number being the temperature in celsius
and the second number is the relative fan speed as a decimal. Note that the fan will
be off if set below `0.25`.
The following is a fan curve with 25% at 60°C, 60% at 90°C, and 100% at 100°C:
```
59,0
60,0.25
90,0.6
100,1
```
