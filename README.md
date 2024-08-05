# Install steps
```shell
sudo apt install flatpak flatpak-builder
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
flatpak install flathub org.kde.Sdk//6.4
flatpak install flathub com.obsproject.Studio//stable
mkdir -p build
```
## Build the package
```shell
flatpak-builder --force-clean build-dir com.obsproject.Studio.Plugin.MultiRtmp.yaml
```

## Install the Package
```shell
flatpak-builder --user --install --force-clean build-dir com.obsproject.Studio.Plugin.MultiRtmp.yaml
```

## Launch the obs Studio Flatpak
```shell
flatpak run com.obsproject.Studio
```
