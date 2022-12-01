# Splashtop for RMM on Linux

Tested with NinjaRMM and Ubuntu 22.04 LTS with wine-7.22 (Staging)

## Requirements

Install WineHQ-staging

```
wget -O- https://dl.winehq.org/wine-builds/winehq.key | gpg --dearmor | sudo tee /usr/share/keyrings/winehq.gpg > /dev/null 2>&1
sudo apt update
sudo apt install --install-recommends winehq-staging -y
```

## Download Splashtop for RMM

Example for Ninja RMM

https://resources.ninjarmm.com/Splashtop/SplashtopForRMM_v3.4.6.1.exe

## Install Splashtop for RMM

```
wine SplashtopForRMM_v3.4.6.1.exe
```

## Add "st-rmm://" handler

```
./register-handler.sh
```

## In case of problems

Clean your previous WINEPREFIX or run in new WINEPREFIX

### Clean your previous WINEPREFIX (DANGER!!!) 

```
rm -rf ~/.wine
```

### Run in new WINEPREFIX

```
WINEPREFIX="$HOME/.myNewWinePrefix"
```

Now change `splashtop-viewer.desktop` to meet requirements.

