# Building using snap:
Add Gamefiles (Blutfest.pck and Blutfest.bin/86_x64) into the Gamefiles folder.

Snap kompilieren schlägt Fehl mit vielen der Internet-Beispiele. Hier der aktuell funktionierende Weg:

Command:
```
sudo SNAPCRAFT_BUILD_ENVIROMENT=host snapcraft
```

For publishing on the snapstore, the confinement should be set to strict.
