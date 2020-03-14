# j

A simple script switching the current Java between installations managed by [SDKMAN](https://sdkman.io/). 
No need to remember the exact identifier nor search the history. Just type `j 8` and use your latest local Java 8.
The script checks for local installations and picks up the latest version of the chosen major Java version.

Checked on macOS 10.15 against SDKMAN 5.7.4 with bash and zsh

## Installation

- Clone the repository (`git clone git@github.com:ldziedziul/j.git`) or download the script (https://raw.githubusercontent.com/ldziedziul/j/master/j.sh)
- Define an alias to make the script use the current shell by adding the following line to your shell config file (`~/.bashrc`, `~/.zshrc`):
```bash
alias j=". ~/projects/j/j.sh"
``` 
- Remember to restart the shell or reload the config file with `source ~/.bashrc` or `source ~/.zshrc`

## FAQ

An alias is needed because normally the script is invoked within the new subshell which makes the change of Java version
 invisible to the parent shell (i.e. the shell you use)
