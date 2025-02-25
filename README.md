# Ubisoft Connect Flatpak (Unofficial)
## Installing
- Download and install WineStaging Flatpaks from https://github.com/ChrisHobday/org.winehq.WineStaging/releases (This Flatpak uses them as a base)
- Download UbisoftConnect.flatpak from releases
- Install UbisoftConnect.flatpak (sudo needed for installing single use Flatpak bundle)
```console
sudo flatpak install UbisoftConnect.flatpak
```
## Launching
- Launch the UbisoftConnect Flatpak (Either search for the app in your menu and click it) or
```console
flatpak run com.ubisoft.UbisoftConnect
```
## Uninstalling
- Remove UbisoftConnect Flatpak
```console
flatpak remove com.ubisoft.UbisoftConnect
```
## Downloading/Cloning this repo
- Click the green button to download zip and extract once downloaded or clone repo with
```console
git clone --recurse-submodules https://github.com/ChrisHobday/com.ubisoft.UbisoftConnect
```
## Building
- Install Flatpak builder
```console
flatpak install flathub org.flatpak.Builder
```
- Install the platform this Flatpak will be using
```console
flatpak install flathub org.freedesktop.Platform//23.08 org.freedesktop.Sdk//23.08
```
- Build the Flatpak with flatpak-builder (Run this from within the com.ubisoft.UbisoftConnect directory)
```console
flatpak run org.flatpak.Builder --force-clean --repo=repo build-dir com.ubisoft.UbisoftConnect.yml
```
## User installation while building
- Replace last Building step with
```console
flatpak run org.flatpak.Builder --force-clean --repo=repo --user --install build-dir com.ubisoft.UbisoftConnect.yml
```
## Building single use Flatpak bundle like in the releases (After having followed the Building steps above)
- Build the Flatpak bundle (Run this from within the com.ubisoft.UbisoftConnect directory after having followed the Building steps above)
```console
flatpak build-bundle repo UbisoftConnect.flatpak com.ubisoft.UbisoftConnect
```
## Troubleshooting
- Check if Flatpak is installed
```console
flatpak list | grep UbisoftConnect
```
- Enter Flatpak in command line mode
```console
flatpak run --command=sh com.ubisoft.UbisoftConnect
```
## Flatpak locations
- Installation directory             = /var/lib/flatpak/app/com.ubisoft.UbisoftConnect/
- Installation directory (User mode) = ~/.local/share/flatpak/app/com.ubisoft.UbisoftConnect/
- User cache directory               = ~/.var/app/com.ubisoft.UbisoftConnect/cache/
- User config directory              = ~/.var/app/com.ubisoft.UbisoftConnect/config/
- User data directory                = ~/.var/app/com.ubisoft.UbisoftConnect/data/
- Wine prefix                        = ~/.var/app/com.ubisoft.UbisoftConnect/data/WinePrefix
