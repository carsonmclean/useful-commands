# Cheatsheet
https://tmuxcheatsheet.com/

# `~/.tmux.conf`
```
# Start windows and panes at 1, not 0
set -g base-index 1
setw -g pane-base-index 1

# Display messages for longer
set -g display-time 4000

# Automatically renumber windows after closing a window
set -g renumber-windows on
```
