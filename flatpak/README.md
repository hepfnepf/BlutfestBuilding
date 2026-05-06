# Updating flatpak

Install flatpack  and add flathub as repo, if not already present on the system. --user macht das alles immer nur für den lokalen User durchgeführt wird, kann evtl. weggelassen werden.

```
sudo apt install flatpak
flatpak remote-add --user flathub https://dl.flathub.org/repo/flathub.flatpakrepo
flatpak install --user org.flatpak.Builder
```

Update by updating manifest and yml. Test building  locally using
```
flatpak run org.flatpak.Builder --force-clean --sandbox --user --install --install-deps-from=flathub --ccache --mirror-screenshots-url=https://dl.flathub.org/media/ --repo=repo builddir io.github.hepfnepf.blutfest.yml
flatpak run io.github.hepfnepf.blutfest
```

Flatpak setup:
https://docs.flatpak.org/en/latest/first-build.html#install-a-runtime-and-the-matching-sdk

Perform a pull request at https://github.com/flathub/io.github.hepfnepf.blutfest.


A decent guide: https://cassidyjames.com/blog/publish-godot-engine-game-flathub-flatpak/
