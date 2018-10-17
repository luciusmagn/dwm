# dwm
My fork of dwm. The following patches have been applied:
* autostart
* pertag
* centeredmaster
* noborder
* bottomstack
* bstackhorizontal

Configuration has been changed to add Alt+O and Alt+U (conflicts with nano editor)
for other changes. See `config.def.h` for my current configuration.

ProFont needs to be installed for this fork of dwm to render properly.
A czech localization of the font is included in the repository.

For the brightness settings to work, isntall `mkdark` and `mklight` into
PATH and the `.dwm` into your home directory.

The two scripts in `.dwm` can be used to auomatically execute commands on
dwm startup.

If you want to get a useful status bar, install `slstatus` or one of those
Go pieces of shit. Alternatively, you can write your own status application
as it is pretty easy, just use `xsetroot -name (stuff)` command to set the
status to whatever you want.

# Original readme:

dwm - dynamic window manager
----------------------------
dwm is an extremely fast, small, and dynamic window manager for X.


Requirements
------------
In order to build dwm you need the Xlib header files.


Installation
------------
Edit config.mk to match your local setup (dwm is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install dwm (if
necessary as root):

    make clean install

If you are going to use the default bluegray color scheme it is highly
recommended to also install the bluegray files shipped in the dextra package.


Running dwm
-----------
Add the following line to your .xinitrc to start dwm using startx:

    exec dwm

In order to connect dwm to a specific display, make sure that
the DISPLAY environment variable is set correctly, e.g.:

    DISPLAY=foo.bar:1 exec dwm

(This will start dwm on display :1 of the host foo.bar.)

In order to display status info in the bar, you can do something
like this in your .xinitrc:

    while xsetroot -name "`date` `uptime | sed 's/.*,//'`"
    do
    	sleep 1
    done &
    exec dwm


Configuration
-------------
The configuration of dwm is done by creating a custom config.h
and (re)compiling the source code.








