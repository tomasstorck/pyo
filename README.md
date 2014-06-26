##############
# Introduction and motivation #
##############
Much like Synapse, Gnome Do, Launchy and some other pieces of software, this program allows you to quickly open another piece of software on your machine or any file by reading a few key strokes and filtering out the matching items. However, while most other launchers sport great feastures, such as maintaining a daemon process in the background, plugins allowing integration with tools like Zeigeist and showing icons of matching items, the aim of this work is to keep it simple, as simple as possible. pyo (PYthon Open) merely creates a database with your programs and files and a database with recently selected items, then integrates all this using dmenu (http://tools.suckless.org/dmenu/).

This must be stressed, pyo is really simple. If you haven't already, try one of the programs listed above, they are more likely to meet your needs. Pyo is a small project I've been working on for a few spare hours to replace Synapse on my personal machines after the latter inexplicitly left out some search results and I could not find out why in a reasonable amount of time.

I'd be happy to add more documentation if you request it. However, because it is unlikely anyone but me will ever use it, I haven't taken the time to do so yet.

#####################
# Quick start guide #
#####################
Before you start, make sure you have all dependencies installed:
* Python 3
* dmenu

Besides these dependencies, only the file pyo is required to run. Put it in a folder that is in your $PATH. Don't forget to make it executable.

You should now be able to run pyo. By running it in the terminal you'll get feedback on its performance and what is going on. Assuming you have not used this program before, there will be no databases available and you'll get an error. Generate empty databases and update the file system database by running in a terminal:

    pyo --dummy --update

This is the minimal amount of setting up you need to do. To summon and use pyo, you'll need to bind it to a shortcut that is globally available. How to add a shortcut key depends on your window manager/desktop environment. Some examples are given below.
COMPIZ: Run ccsm, go to Commands and add a command line for pyo. Under the tab Key Bindings, add a shortcut key.
LXQT:   Open the global key configuration screen (e.g., run lxqt-config-globalkeyshortcuts in the terminal). The type you're looking for is Command, not DBus
The command you want to bind a shortcut key to depends on you. For example, you could do a database update every time after pyo finishes, by using:

    pyo -o -u

###################
# Tricks and tips #
###################
1.  The script is quite customisable: just open the file in a text editor and change your settings in the configuration section
2.  You can add arguments to the selected entry. Press TAB to fill in the selected item, add your extra arguments and  press ENTER. For example, to use interactive mode for gnome-screenshot, type "screens", press TAB, type " -i". This entry is automatically stored in the recent database
3.  Use SHIFT+ENTER to execute the command as entered, not filling in the selected item

###########
# License #
###########
You're welcome to use anything in here, as long as you pass useful improvements forward. Therefore, this product is licensed under the GPL v3 license. The content of this license is readily available, for example via http://www.gnu.org/copyleft/gpl.html
