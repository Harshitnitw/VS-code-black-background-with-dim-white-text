Add `claude-dim` wrapper in your codebase

Quick setup:
1. Create the wrapper script: `touch claude-dim`
2. Paste the following content in it. You may open it with `code claude-dim`
```
#!/bin/bash
# Claude Code wrapper to dim bright white text

# Function to process output and dim bright white colors
process_output() {
    sed 's/\x1b\[97m/\x1b[90m/g; s/\x1b\[1;37m/\x1b[90m/g; s/\x1b\[0;97m/\x1b[90m/g; s/\x1b\[1;97m/\x1b[90m/g; s/\x1b\[37;1m/\x1b[90m/g; s/\x1b\[1m\x1b\[37m/\x1b[90m/g; s/\x1b\[37m/\x1b[90m/g; s/\x1b\[0;37m/\x1b[90m/g; s/\x1b\[38;5;15m/\x1b[90m/g; s/\x1b\[38;5;7m/\x1b[90m/g'
}

# If no arguments, force interactive mode
if [ $# -eq 0 ]; then
    # Use expect or script to handle interactive session
    script -q /dev/null -c "claude" | process_output
else
    # For commands with arguments
    claude "$@" 2>&1 | process_output
fi
```
3. Make executable: chmod +x claude-dim
4. Apply the JSON user settings shared in the repo

Then use: `./claude-dim` instead of `claude`
