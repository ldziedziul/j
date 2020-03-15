# j

A simple script switching the current Java between installations managed by [SDKMAN](https://sdkman.io/). 

No need to remember the exact identifier nor search the history. Just type `j 13` and use your latest local Java 13. 
The script checks for local installations and picks up the latest version of the chosen major Java version.

Checked on macOS 10.15 against SDKMAN 5.7.4 with bash and zsh

```bash
$ j
Available versions:
13
11
8
Current: 11
Usage: j <java_version>

$ j 8
Using java version 8.0.242.hs-adpt in this shell.
```

## Installation

- Clone the repository (`git clone git@github.com:ldziedziul/j.git`) or download the script (https://raw.githubusercontent.com/ldziedziul/j/master/j.sh)
- Define an alias to make the script use the current shell. Add the following line to your shell config file (`~/.bashrc`, `~/.zshrc`):
```bash
alias j=". ~/projects/j/j.sh"
``` 
- Remember to restart the shell or reload the config with `source ~/.bashrc` or `source ~/.zshrc`

## Usage
Run `j` without arguments to see all local Java versions installed by SDKMAN. 

Run `j <version>` to switch the current shell to the latest local Java version of your choice.

## FAQ

- **Why do I need to set up the alias and not simply use the script directly?**
The alias is required because normally the script is invoked within the new subshell which makes the change of Java version
 invisible to the parent shell (i.e. the shell you use). The dot in the alias means the script will be run within the current shell.
