# My build of st
The following patches have been added (found in the patches folder)
+ alpha
+ anysize
+ bold-is-not-bright
+ boxdraw_v2
+ externalpipe
+ externalpipe-eternal
+ font2
+ iso14755
+ ligatures
+ scrollback
+ scrollback-mouse
+ scrollback-mouse-altscreen
+ vertcenter
+ xresources
+ xclearwin
+ clipboard

Keybindings have also been customised to my tastes. Checkout config.def.h for more.
Version 0.8.4.

st - simple terminal
--------------------
st is a simple terminal emulator for X which sucks less.


Requirements
------------
In order to build st you need the Xlib header files.


Installation
------------
Edit config.mk to match your local setup (st is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install st (if
necessary as root):

    make clean install


Running st
----------
If you did not install st with make clean install, you must compile
the st terminfo entry with the following command:

    tic -sx st.info

See the man page for additional details.

Credits
-------
Based on Aurélien APTEL <aurelien dot aptel at gmail dot com> bt source code.

