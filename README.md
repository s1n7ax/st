# st - simple terminal
st is a simple terminal emulator for X which sucks less.

![Screeshot](screenshots/1.png?raw=true "Screenshot 1")

## Features
This is a custom build of `git clone https://git.suckless.org/st` preloaded with few patches really necessary for regular use.
Patches:
* st-alpha
	* transparent terminal windows
	* `xcompmgr` should be running this to effect
* st-dracula
	* famous dracula theme
* st-externalpipe
	* pipe read or write st screen
	* awesome feature if you make use of it
* st-fix-keyboard-input
	* this allowing more fancy key combination
	* more shortcuts for `vim`
* st-scrollback-mouse-altscreen
	* scroll back through the logs
	* use `mouse` scroll or `shift+page up/down`

## Requirements
In order to build st you need,
(Ubuntu)
```
sudo apt install make gcc build-essential libx11-dev libxft-dev fonts-fantasque-sans
```

## Installation
Edit `config.mk` to match your local setup (st is installed into
the /usr/local namespace by default).

You will find all the configurations in `config.def.h` .

Afterwards enter the following command to build and install st (if
necessary as root):
```
make clean install
## or
sudo make clean install
```

## Running st
If you did not install st with make clean install, you must compile
the st terminfo entry with the following command:

```
tic -sx st.info
```

See the man page for additional details.

## Credits
Based on Aurélien APTEL <aurelien dot aptel at gmail dot com> bt source code.


