##############
# Introduction and motivation #
##############
Much like Synapse, Gnome Do, Launchy and some other software, this program allows you to quickly open another piece of software or file on your machine by filtering out the matching items as you type.
However, while most other launchers sport great extra features, such as maintaining a daemon process in the background, plugins allowing integration with tools like Zeigeist and showing icons of matching items, the aim of this work is to keep it simple. pyo (PYthon Open) creates a database in advance with your programs and files and a database with recently selected items, then presents these using dmenu (http://tools.suckless.org/dmenu/).

I'd be happy to add more documentation if you request it. However, because it is unlikely anyone but me will ever use it, I haven't taken the time to do so yet.

#####################
# Quick start guide #
#####################
Before you start, make sure you have all dependencies installed:
* Python 3
* dmenu

Besides these dependencies, only the file pyo and settings file are required to run the program. Put pyo in a folder that is in your `$PATH` (don't forget to make it executable) and put the settings file in `~/.config/pyo/`

To summon and use pyo, you'll need to bind it to a shortcut that is globally available. How to add a shortcut key depends on your window manager/desktop environment. Some examples are given below.

* COMPIZ: Run `ccsm`, go to Commands and add a command line for pyo. Under the tab Key Bindings, add a shortcut key.

* LXQT:   Open the global key configuration screen (e.g., run `lxqt-config-globalkeyshortcuts` in the terminal). The type you are looking for is Command, not DBus

The command you want to bind a shortcut key to depends on you. For example, you could do a database update after pyo finishes opening a file, by using:

    pyo -o -u

###################
# Tricks and tips #
###################
1.  The script is quite customisable: just open the file in a text editor and change your settings in the configuration section
2.  You can add arguments to the selected entry. Press TAB to fill in the selected item, add your extra arguments and  press ENTER. For example, to use interactive mode for `gnome-screenshot`, type "screens", press TAB, type " -i". This entry is automatically stored in the recent database. This way you can store and use nice one-liners.
3.  Use SHIFT+ENTER to execute the command as entered, not filling in the selected item

###########
# License #
###########
This product is licensed under the GPL v3 license. The content of this license is readily available, for example via http://www.gnu.org/copyleft/gpl.html
