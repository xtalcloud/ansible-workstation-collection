# Ansible Enterprise Linux Workstation Collection

This Ansible Collection is meant to be used with a fresh install of EL 8. It was built testing on RHEL8 & Rocky Linux 8.

It includes a minimal GUI and many common command line tools common in terminal-based workflows.

These roles were designed with IT admin machines in mind. They are highly customized with tooling that allow for IT administrators to quickly navigate between various shells on various machines while still running a machine that is not bloated with software that comes in a default EL8 installation.

## User Interace

For the sake of explanation, assume that the user interface, from here on UI, is mainly the coordinated operation of these 4 tools:

1. Window Manager
2. Window Compositor
3. Terminal emulator
4. Shell

Items 1 through 3 in this list constitute the "graphical" component of the UI, and will be refered to as the GUI from here on out. The operation of these 3 items in this "spin" of Enterprise Linux is exteremely intertwined. For this reason, these 3 roles will always be run together on any hosts.

The shell, while the focal point of the UI, is operates indepently from these 3 components. For this reason, it along with things like text editor configuration fall in the realm of things which the particular user may configure without fear of breaking the graphical component of the UI.

### Minimal (G)UI

I put the letter "G" in parenthesis here becaues the purpose of installing an X server and Window Manager with these Ansible roles is *NOT* to provide a desktop environment that will allow users to run graphical applications like Chrome or Wireshark (however it will).

The purpose is to enhance a terminal-based workflow by adding some of the niceities afforded by running a window manager, like the ability to have multiple terminals tiled accross one's desktop, supporting mulitiple monitors, being able to run a transparent terminal over another window containing a manual or documentation underneath that you can read, etc.

That being said, the ability to run a browser along side all your terminal/editor windows is a huge bonus.

For this "spin" of Enterprise Linux, I've chosen the following implementations of the components listed above as graphical components of the UI:

1. Window Manager: *dwm*
2. Window Compositor: *compton*
3. Terminal emulator: *st*

#### Window Manager
#### Window Compositor
#### Terminal Emulator

Customized versions of the suckless tools dwm & st have been included. The original C source code can be found at:

* https://github.com/kriipke/st.git
* https://github.com/kriipke/dwm.git

If you'd like to customize them further see https://st.suckless.org/ & https://dwm.suckless.org/, respectively.

### Featureful CLI

* zsh
* neovim
