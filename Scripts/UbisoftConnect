#!/bin/sh
echo "Checking if Ubisoft Connect is already installed"
if [ -d "/var/data/wine/drive_c/Program Files (x86)/Ubisoft/Ubisoft Game Launcher" ]; then
  echo "Ubisoft Connect is installed"

  echo "Setting up Discord rich presence"
  for i in {0..9}; do
      test -S $XDG_RUNTIME_DIR/discord-ipc-$i ||
      ln -sf {app/com.discordapp.Discord,$XDG_RUNTIME_DIR}/discord-ipc-$i;
  done

  echo "Changing directory to /var/data/wine/drive_c/Program Files (x86)/Ubisoft/Ubisoft Game Launcher"
  cd /var/data/wine/drive_c/Program\ Files\ \(x86\)/Ubisoft/Ubisoft\ Game\ Launcher/

  # TODO: Find out why and fix Ubisoft Connect failing to launch after installed
  echo "Launching Ubisoft Connect"
  wine /var/data/wine/drive_c/Program\ Files\ \(x86\)/Ubisoft/Ubisoft\ Game\ Launcher/UbisoftConnect.exe
else
  echo "Ubisoft Connect is not installed"

  echo "Initializing Wine prefix"
  wineboot -i

  echo "Launching Battle.netSetup.exe"
  wine /app/bin/UbisoftConnectInstaller.exe
fi