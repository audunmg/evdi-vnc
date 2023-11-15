# evdi-vnc
A minimalist utility to start up a VNC server as a secondary screen using EVDI.

# Usage
Make sure the evdi kernel module is loaded with: `modprobe evdi`

Run: `sudo ./evdi-vnc`

On another device connect with any standard vnc client. Tigervnc or tightvnc on linux seems to give the best performance.

There is a bug, which requires you to rmmod and modprobe evdi every time evdi-vnc is restarted.

It starts up with high resolution mode 3820x2160, which works well on 10G network. For gigabit, that's very laggy, and 2560x1440 is better. Change resolution on the virtual screen as if it was a normal screen.


# Building
Simply run `make`

# Dependencies
evdi-vnc has only two dependencies: [libvncserver](https://github.com/LibVNC/libvncserver) and
[evdi](https://github.com/DisplayLink/evdi).

libvncserver can likely be installed from your package manager.

libevdi is currently statically linked with evdi-vnc, but you'll also need install the evdi
kernel module in order to use evdi-vnc.

# License
This code is licensed under the GNU Public License v2. See the LICENSE for the full license text.
