Much like Synapse, Gnome Do, Launchy and some other pieces of software, this program allows you to quickly open another piece of software on your machine or any file in your home partition by reading a few key strokes and filtering out the matching items. However, while most other launchers sport great feastures, such as maintaining a daemon process in the background, allowing extension through plugins, showing icons of matching items and integration with tools like Zeigeist, the aim of this work is to keep it simple, as much as possible. Pyo merely creates a database with your programs and files, then integrates with dmenu (http://tools.suckless.org/dmenu/) to filter out matching items and open the selected files.

This must be stressed, pyo is really simple. If you haven't already, try one of the programs listed above, they are more likely to meet your needs. Pyo is a small project I've been working on for a few spare hours to replace Synapse on my personal machines after the latter inexplicitly left out some search results.

Perhaps pyo is useful for you, perhaps you can use some bits of this code for your own project, or used it to improve your knowledge of Python. Perhaps you like the idea and developed something better. Either way, I'd really appreciate a message if you find any use for the code used in this project, or if you have an idea how to improve it while keeping it simple. Please contact me through tomasvandenooijevaer@gmail.com. 

I'd be happy to add more documentation if you request it. However, because it is unlikely anyone but me will ever use it, I haven't taken the time to do so yet.



#####################
# Quick start guide #
#####################
Before you start, make sure you have all dependencies installed. This should be as simple as installing Python 3 and dmenu, no other libraries should be required.

Because only a single file is required to run pyo, the easiest way to download it manually from GitHub: copy the contents of the file https://raw.githubusercontent.com/tomasstorck/pyo/master/pyo to a file named pyo somewhere in your $PATH. Be sure to make this file executable, for example using:
    chmod +x pyo

Assuming you have not used this program before, there will be no databases available. Generate empty databases and update the file system database by running in a terminal:
    pyo --dummy --update

To summon pyo, you'll need to bind it to a shortcut that is globally available. How to add a shortcut key depends on your window manager/desktop environment. Some examples are given below.
COMPIZ: Run ccsm, go to Commands and add a command line for pyo. Under the tab Key Bindings, add a shortcut key.
LXQT:   Open the global key configuration screen (e.g., run lxqt-config-globalkeyshortcuts in the terminal). The type you're looking for is Command, not DBus

The command you want to bind a shortcut key for depends on you. Ideally, you'd update the file system database every time you run, but this way it can take seconds before pyo is shown. Instead, you could do the database update after pyo finishes, by using:
    pyo -o -u
    
    
###########
# License #
###########
You're welcome to use anything in here, as long as you pass useful improvements forward. Therefore, this product is licensed under the GPL v3 license. The content of this license is readily available, for example via http://www.gnu.org/copyleft/gpl.html
