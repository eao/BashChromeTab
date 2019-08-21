# BashChromeTab
For Unix systems.  If Chrome not open, opens Chrome.  If Chrome is open, sends Ctrl+T to the topmost window, opening a new tab with the default keybindings.

First, numberofwindows is set to the number of windows of Chrome open.  If > 0, the topmost window has Ctrl+T send to it.  The topmost window is selected using numberofwindows - xdotool's window stack is indexed starting with the bottommost window at 1, so the topmost window's index in the stack is equal to the number of windows.  I don't understand what the "--window 0" bit does but it doesn't seem to work without it.

If the number of windows is 0, then Chrome is opened with nohup.  Nohup message avoided by copy-pasting a code snippet from https://stackoverflow.com/questions/10408816/how-do-i-use-the-nohup-command-without-getting-nohup-out?newreg=7846db1d3a054c5b94db53386885b3c2.  I don't fully understand how it works.
