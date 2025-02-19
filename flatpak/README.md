# Updating flatpack
Update by updating manifest and yml. Test building  locally using
```
flatpak run org.flatpak.Builder --force-clean --sandbox --user --install --install-deps-from=flathub --ccache --mirror-screenshots-url=https://dl.flathub.org/media/ --repo=repo builddir io.github.hepfnepf.blutfest.yml
```

Perform a pull request at https://github.com/flathub/io.github.hepfnepf.blutfest.


A decent guide: https://cassidyjames.com/blog/publish-godot-engine-game-flathub-flatpak/
