# ShellExtender
This project modify and extend ZSH or BASH shell about some new functionality.

* Defines aliases (see **aliases** file)
  * Filesystem aliases as **ll, ls, ..** etc.
  * **grep** colorization
  * **servethis** - spawn a simple HTTP server on port 8000 serving the current directory
  * **pypath** - print your python path, minus all the egg files
  * **pycclean** - recursively clean out all of the pyc files from current directory
  
  And more...

* Defines some useful functions
  * **extract file** - extracts file archive. Choose extractor by file extension Defined only when zsh plugin or sytem command doesn't exist
  * **dls [dir]** - list sub-directories in dir
  * **dla [dir]** - list all sub-directories in dir included .dot files
  * **dgrep pattern** - recursive, case-insensitive grep that excludes binary files
  * **dfgrep pattern** - recursive, case-insensitive grep that excludes binary files and returns only unique filenames
  * **psgrep pattern** - grep for all processes match specified pattern
  * **killit pattern** - kills any process that matches a regexp passed to it
  * **tree [dir]** - dumps tree file structure from specified dir. Defined only when system command tree isn't installed
  * **mcd dir** - makes a dir and cd into it
  * **exip** - dumps current public IP address
  * **ips** - dumps local IP addresses
  * **shell** - dumps the shell what you are using

* Defines some global variables (see the **variables** file)
  * **PATH** variable
  * **MANPATH** variable
  * **INFOPATH** variable
  * Preferred editor by **EDITOR** variable
  * *grep* colorized output
  * Variables to modify **less** command behavior
  * Shell **history** parameters variables
  * Escape sequences for **formatting** and **colorize** shell output
  
* Fire new or attach to existing TMUX session when connected through SSH

##How to enable 
1. Create any sub-folder in your home directory (.shell_extender)
2. Copy project content to the directory
3. Modify **config** file in the directory to fit your needs
4. Append following sniplet at the end of your .zshrc or .bashrc file

```bash
SHELL_EXTENDER_DIR=~/.shell_extender

if [[ -f "$SHELL_EXTENDER_DIR/shell_extender" ]]; then
   . "$SHELL_EXTENDER_DIR/shell_extender"
fi
```
5. Enjoy new functionality
