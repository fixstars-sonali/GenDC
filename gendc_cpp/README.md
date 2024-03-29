## Window

### Setup

- vcpkg (Pre-req)

```
git clone https://github.com/microsoft/vcpkg.git
cd vcpkg
.\bootstrap-vcpkg.bat
```

- Install Gstreamer

```
cd .\gendc_cpp\
<path-to-vcpkg.exe> install

$env:PKG_CONFIG_PATH="C:\WorkSpace\Sensing-Dev\sonali\GenDC\gendc_cpp\vcpkg_installed\x64-windows\lib\pkgconfig;$env:PKG_CONFIG_PATH"  
```

### Build

- Use ninja

```
meson setup ../build
ninja -C build
```

- Use visual studio as back end

```powershell
 meson setup ../build --backend vs2022 -Dtests=enabled --pkg-config-path "C:\WorkSpace\Sensing-Dev\sonali\GenDC\gendc_cpp\vcpkg_installed\x64-windows\lib\pkgconfig" 
 ```

- reconfigure 
 ```
 meson setup ../build --backend vs2022  --reconfigure -Dtests=enabled --pkg-config-path "C:\dev\vcpkg\installed\x64-windows\lib\pkgconfig"  
```

### Inspect

```powershell
$env:GST_PLUGIN_PATH="$env:GST_PLUGIN_PATH;d:\Workspace\Sensing-Dev\GenDC\build\gst\gendcparse"
```
```powershell
gst-inspect-1.0 gendcparse
```

## Ubuntu

### Setup

- Install Gstreamer

```
apt-get install libgstreamer1.0-dev libgstreamer-plugins-base1.0-dev libgstreamer-plugins-bad1.0-dev gstreamer1.0-plugins-base gstreamer1.0-plugins-good gstreamer1.0-plugins-bad gstreamer1.0-plugins-ugly gstreamer1.0-libav gstreamer1.0-tools gstreamer1.0-x gstreamer1.0-alsa gstreamer1.0-gl gstreamer1.0-gtk3 gstreamer1.0-qt5 gstreamer1.0-pulseaudio
```

### Build

- Use ninja

```
meson setup ../build
ninja -C build
```

### Test
- Run tests 

```
meson test -C ../build/
```




