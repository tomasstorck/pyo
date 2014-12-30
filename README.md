##############
# Introduction and motivation #
##############
Much like Synapse, Gnome Do, Launchy and some other software, this program allows you to quickly open another piece of software or file on your machine by filtering out the matching items as you type.
However, while most other launchers sport great extra features, such as maintaining a daemon process in the background, plugins allowing integration with tools like Zeigeist and showing icons of matching items, the aim of this work is to keep it as simple as possible. `pyo` (PYthon Open) maintains a database with your programs and files and a database with recently selected items, then presents these using `dmenu` (http://tools.suckless.org/dmenu/).

#####################
# Quick start guide #
#####################
Before you start, make sure you have all dependencies installed:
* Python 3
* dmenu

Besides these dependencies, only the file `pyo` is required to run the program. Put `pyo` in a folder that is in your `$PATH` (don't forget to make it executable).

To summon and use `pyo`, you'll need to bind it to a shortcut that is globally available. How to add a shortcut key depends on your window manager/desktop environment. Some examples are given below.

* COMPIZ: Run `ccsm`, go to Commands and add a command line for `pyo`. Under the tab Key Bindings, add a shortcut key.

* LXQT:   Open the global key configuration screen (e.g., run `lxqt-config-globalkeyshortcuts` in the terminal). The type you are looking for is Command, not DBus

The command you want to bind a shortcut key to depends on you. For example, I do a database update after `pyo` finishes opening a file, by using:

    pyo -o -u

###################
# Tricks and tips #
###################
`dmenu` is where most of the magic happens, so be sure to read the manpages (http://man.cx/dmenu)
1.  The script is quite customisable: most settings can be changed by editing `~/.config/pyo/settings`
2.  You can add arguments to the selected entry. Press `TAB` to fill in the selected item, add your extra arguments and  press `SHIFT-ENTER`. For example, to use interactive mode for `gnome-screenshot`, type `screens`, press `TAB`, type ` -i` and press `SHIFT-ENTER` to execute this line (with `SHIFT` because this is a new enty; see `dmenu` manpages). This entry is automatically stored in the recent database. This way you can store and use nice one-liners.
3.  Run `pyo` in a terminal to evaluate speed bottlenecks or error messages

###########
# License #
###########
This product is licensed under the GPL v3 license. The content of this license is readily available, for example via http://www.gnu.org/copyleft/gpl.html
