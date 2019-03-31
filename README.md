# manjaro-setup

Documenting my manjaro setup process.
I prefer KDE because it is lightweight and very customizable. 

## First steps after installation

Install `pamac`, remove `octopi` and related packages. Enable AUR sources in pamac settings.
Download `adapta` theme for KDE and GTK. Set theme options in `System Settings/Appearance`. 

## Scaling content on small display

I use a Dell XPS 13 and thus have a relatively small screen. With default settings, text is barely readable. 
I recommend *not* to use the `Scale display` or `Force font dpi` options as recommended in other guides. The reason for this is that some apps (Qt based?) fail to render fonts correctly. 
Instead, I recommend just increasing all font sizes by 2 to 3 points in `Fonts` settings.
