# Building using snap:

### Ininit if not happend yet:
Create a folder (Here "Blutfest"). Run sudo snapcraft init in it.

### Files structure
Add Gamefiles (Blutfest.pck and Blutfest.bin/86_x64) into the Gamefiles folder. And replace the snapcraft.yaml that was created in the init step with the snapcraft.yaml in this repo.

```
- Blutfest
-- gamefiles
--- Blutfest.pck
--- Blutfest.bin/86_x64
-- snap
--- snapcraft.yaml
```


> [!IMPORTANT]  
> The files in gamefiles need to have the final rights. You can give all rights using chmod 777 *
> If you have already build a snap before setting the correct permissions, you need to run sudo snapcraft clean!


### Create the snap
Normaly, running this command in the Blutfest folder should work:
```
sudo snapcraft
```
Sometimes it failes and you need to run this command instead:

Command:
```
sudo SNAPCRAFT_BUILD_ENVIROMENT=host snapcraft
```

### Publish
Run 

```
snapcraft login
```

and 

```
snapcraft upload --release=stable blutfest_0.4.2_amd64.snap
```

where --release is the channel for it.

For publishing on the snapstore, the confinement should be set to strict.
