# poll-cop
poll-cop is an osx utility for receiving notifications that a process has
completed execution AFTER the process has already begun. 

## Usage
If after starting a process, such as `sudo make install`, and letting it run for a bit, you
realize the process may take longer than you expected to finish,
all you have to do in order to recieve a notification on its
completion is (in fish)
```
> sudo make install
(CTRL-Z)
> echo %
12345
> watch 12345
> fg
```
And once `sudo make install`, or whatever you happen to running, completes you
will recieve a native notification on your screen so you don't have to keep
checking the terminal.
## Requirments
- `reattach-to-user-namespace`
    - Install with `brew install reattach-to-user-namespace`. This is used to
      fix issues with running applescript in a tmux session

## To do
- [ ] Make `reattach-to-user-namespace` an optional dependency
- [ ] Add optional sound to notification
- [ ] Add support for various linux distros
