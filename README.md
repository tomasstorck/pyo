##############
# Introduction and motivation #
##############
Much like Synapse, Gnome Do, Launchy and some other software, this program allows you to quickly open another piece of software or file on your machine by filtering out the matching items as you type.
However, while most other launchers sport great extra features, such as maintaining a daemon process in the background, plugins allowing integration with tools like Zeigeist and showing icons of matching items, the aim of this work is to keep it as simple as possible. `pyo` (PYthon Open) maintains a database with your programs and files and a database with recently selected items, then presents these using `dmenu` and opens the selected entry with `xdg-open`.

#####################
# Quick start guide #
#####################
Before you start, make sure you have all dependencies installed:
* Python 3
* [dmenu](https://wiki.archlinux.org/index.php/Dmenu)
* [xdg-tools] (https://wiki.archlinux.org/index.php/Xdg-open) 

Besides these dependencies, only the file `pyo` is required to run the program. Put `pyo` in a folder that is in your `$PATH` (don't forget to make it executable).

To summon and use `pyo`, you'll need to bind it to a shortcut that is globally available. How to add a shortcut key depends on your window manager/desktop environment. Some examples are given below.

* GNOME:  See https://help.gnome.org/users/gnome-help/stable/keyboard-shortcuts-set.html.en
* KDE:    See https://userbase.kde.org/System_Settings/Shortcuts_and_Gestures
* LXQT:   Open the global key configuration screen (e.g., run `lxqt-config-globalkeyshortcuts` in the terminal). The type you are looking for is Command, not DBus
* COMPIZ: Run `ccsm`, go to Commands and add a command line for `pyo`. Under the tab Key Bindings, add a shortcut key.

The command you want to bind a shortcut key to depends on you. For example, I do a database update *after* `pyo` finishes opening a file, by using:

    pyo -o -u

#######
# FAQ #
#######
**Why does everything open in Firefox?**

This is a known oddity in `xdg-open`. Add `export DE=gnome` to your `~/.xinitrc` to fix this, even if you don't use GNOME.

**How can I start a program with arguments?**

Press `TAB` to fill in the selected item, add your extra arguments and press `SHIFT-ENTER`. For example, to use interactive mode for `gnome-screenshot`, type `screens`, press `TAB`, type ` -i` and press `SHIFT-ENTER` to execute this line as it is written. See the man files for dmenu for more information (http://man.cx/dmenu).

**Why does nothing happen?/Why is pyo so slow?**

Run `pyo` in a terminal to evaluate speed bottlenecks or error messages

**How can I change the looks of the program?**

pyo is quite customisable: most settings can be changed by editing `~/.config/pyo/settings`

###########
# License #
###########
This product is licensed under the GPL v3 license. The content of this license is readily available, for example via http://www.gnu.org/copyleft/gpl.html
