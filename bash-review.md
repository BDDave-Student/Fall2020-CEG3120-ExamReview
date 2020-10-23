## Bash

- IO redirection: \> and \<
- Different types of quotes: ' vs "
- ~/.bashrc vs ~/.profile: Environment-based vs Local-user based
- source vs ./ vs running script using name: 
- `The terminal you are in is a process.  That process also uses your configuration files as they were when you logged in / opened the terminal.  When you run the script using ./ Or via the command name, it runs as its own process (think virtual window).  You could toss in a sleep command and see it sitting there with ps.  Because the script is it's own process, .bashrc is getting reloaded, but not for your shell - for the virtual shell.`
- ` ./ for script is a direct path to a file name`
- ` script name uses implied $PATH env var if file found` 
- `Source Keyword uses current working shell/terminal - any command ran in script, activates on screen`
- Variables and accessing variable values: varName vs $varName ($ is for usage)
- Use arguments: using scriptname $1  vs $1 inside bash script inside function
  - In a script
  - In a script function
- Conditionals (using the `test` command):  \[ vs \[\[ - Single for Keywords, Double for Keywords + arithmetic compares, use with && echo true/false 
- if statements: if \[ conditional ]; then statement; fi
- functions
