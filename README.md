# manjaro-setup

Documenting my manjaro setup process.
I prefer KDE because it is lightweight and very customizable. 

## First steps after installation

Install `pamac`, remove `octopi` and related packages. Enable AUR sources in pamac settings.
Download `Qogir` theme for KDE, GTK and kvantum. Set theme options in `System Settings/Appearance`.
Download and apply `qogir-icons`.

Change `Removable devices` settings so data partitions are mounted on login. Alternative: Use `gnome-disk-utility` and edit mount options.

Enable `TRIM` support by running `sudo systemctl enable fstrim.timer`. This will clean up deleted files once a week.

## Scaling content on small display

I use a Dell XPS 13 and thus have a relatively small screen. With default settings, text is barely readable. 

### KDE

I recommend *not* to use the `Scale display` or `Force font dpi` options as recommended in other guides. The reason for this is that some apps (Qt based?) fail to render fonts correctly. 
Instead, I recommend just increasing all font sizes by 2 to 3 points in `Fonts` settings.

### XFCE

For XFCE, the DPI can be adjusted (recommended: 120) in the `Settings Editor` under `xsettings/xft`. To fix titlebar size, download [adapta XFWM4](https://www.xfce-look.org/p/1262068/) which has much larger buttons than the default adapta theme.

Terminal colors: [base16 pack](https://github.com/afq984/base16-xfce4-terminal/tree/master/colorschemes).
Recommended preset for adapta: One Dark or Material

Windows-like taskbar icons with launcher: [DockBarX](https://github.com/M7S/dockbarx)

### Firefox

Scaling can be adjusted by setting the `layout.css.devPixelsPerPx` property in `about:config`. Recommended: 1.2 or 1.25

## Shortcuts

Change global shortcuts so `Super` + `T` opens a terminal. Set `Super` + `Left` / `Right` to switch through Desktops.

Add Keyboard layout for German Umlaute: `Language: English`, `Layout: EurKEY`. This makes it so most special characters can be accessed with `Right Alt`.

Use `gnome disk utility` to enable automounting data partitions on login. 

## Package manager optimization

Follow the steps described in the [ArchWiki](https://wiki.archlinux.org/index.php/Makepkg#Utilizing_multiple_cores_on_compression) to speed up the installation of AUR packages.

## Undervolting for laptops

It is possible to undervolt my CPU on my laptop using `python-undervolt` and `throttled` packages.
