# Ubisoft Connect (Unofficial)
## Building
> **_NOTE:_**  With org.winestaging.Sdk and org.winestaging.Platform installed.
```console
flatpak run org.flatpak.Builder build-dir --repo=../Compatpak/repo --force-clean com.ubisoft.UbisoftConnect.yml
```
## Installing
```console
flatpak install --user ../Compatpak/repo com.ubisoft.UbisoftConnect
```
## Running
```console
flatpak run com.ubisoft.UbisoftConnect
```
## Removing
```console
flatpak remove com.ubisoft.UbisoftConnect
```
## Troubleshooting
- Check if Flatpak is installed
```console
flatpak list | grep Ubisoft
```
- Enter Flatpak in command line mode
```console
flatpak run --command=sh com.ubisoft.UbisoftConnect
```
## Flatpak locations
- Installation directory             = /var/lib/flatpak/app/com.ubisoft.UbisoftConnect/
- Wine prefix                        = ~/.var/app/com.ubisoft.UbisoftConnect/data/wine
