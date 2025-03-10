# Edge Bevel

A new bevel algorithm for GIMP that uses difference of gaussians edge detect and other things.

![image](https://github.com/user-attachments/assets/880ffc7b-c159-49e1-9a2b-180000e584ce)

![image](https://github.com/user-attachments/assets/9d25c6d2-56cc-4f58-9efa-66cd99f67460)



## Directory to put Binaries (They do NOT go in the normal plugins folder)

**Windows**

 `C:\Users\(USERNAME)\AppData\Local\gegl-0.4\plug-ins`

 **Linux**

`~/.local/share/gegl-0.4/plug-ins`

 **Linux (Flatpak includes Chromebook)**

`~/.var/app/org.gimp.GIMP/data/gegl-0.4/plug-ins`

Then Restart Gimp and go to "GEGL Operation" and look for "Ocean's Surface 2". Gimp 2.99.16+ users will find the filter in Filters>Text Styling , where as 2.10 plugins will only be found in the drop down list.


## Compiling and Installing

### Linux

To compile and install you will need the GEGL header files (`libgegl-dev` on
Debian based distributions or `gegl` on Arch Linux) and meson (`meson` on
most distributions).

```bash
meson setup --buildtype=release build
ninja -C build

```

### Windows

The easiest way to compile this project on Windows is by using msys2.  Download
and install it from here: https://www.msys2.org/

Open a msys2 terminal with `C:\msys64\mingw64.exe`.  Run the following to
install required build dependencies:

```bash
pacman --noconfirm -S base-devel mingw-w64-x86_64-toolchain mingw-w64-x86_64-meson mingw-w64-x86_64-gegl
```

Then build the same way you would on Linux:

```bash
meson setup --buildtype=release build
ninja -C build
```

  
  ## More previews of this based plugin
  
![image](https://github.com/user-attachments/assets/34207e19-dfd4-4280-89e9-326c322ca39f)

![image](https://github.com/user-attachments/assets/abe4a092-31ea-4268-a2b7-35d2c6ffc43a)

