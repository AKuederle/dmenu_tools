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