# Dmenu_tools

A little repository, where I collect small dmenu scripts I am using (currently 3 xD).

## Win_switcher

A small script, which allows to change the active window (similar to alt+Tab in most of the Wmm) using dmenu and wnctrl. I simply lists all currently active windows and let you select a window in the typical dmenu way.

### Dependency

Dmenu and wnctrl (and a Window manager, which is supported by winctrl)

### Future Plans

Add a filter, so that Desktop and the quake console are not displayed in the list.

## Git_jumper

Git_jumper is a small script, which uses dmenu to let you quickly jump to any git repository on your PC.

It creates a dictionary containing the foldername and folderpath of all git repositories on the computer. (Warning: If you have a great number of repositories this might be slow!) The list of foldernames is then piped to dmenu. Based on the users selection, a terminal with its working directory set to the respective folder gets opened.

### Dependency

Obviously you need to have dmenu installed on your machine.

### Customisation

#### Exclude git repos

You can simply limit the search to certain folders by calling the find command with additional arguments (see man find)

#### Change the action

To change what happens with selected git repo you can easily replace the command inside the if statement with whatever you want (open different terminal, open file browser, open your texteditor ...). The path to the selected git repo can be obtained using : "${gitdic["$choice"]}"

## Dmenu_shutdown 

Dmenu_shutdown is a simple script to logout, hibernate, shutdown, sleep, or restart.

### Dependency

Obviously you need to have dmenu installed on your machine.

### Customisation

Before using the script it has to be customized for your specific system. Add the logout command for your WM and use different shutdown/hibernate commands, if your are using a powermanagment tool.