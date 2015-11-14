# SendText+ for Sublime Text

This package improves [SendText](https://github.com/wch/SendText), particularly for `r`,
`python` and `julia` syntaxes. It supports 

 - Terminal and iTerm on Mac
 - screen and tmux on Unix machines
 - [Cmder](http://cmder.net) and Cygwin on Windows (see below to configure Cmder)
 - SublimeREPL for R and python syntaxes (it works better with R)

Terminal is the default for Mac, Cmder for Windows and tmux for Linux. To change the default program, launch `SendText+: Choose Program` in command palatte.


### Installation

Via Package Control.

### Usage

- <kbd>cmd</kbd>+<kbd>enter</kbd> (Mac) or <kbd>ctrl</kbd>+<kbd>enter</kbd> (Windows/Linux)

    If text is selected, it sends the text to the program selected. If no text is selected, then it sends the current block (if found). Finally, it moves the cursor to the next line.


- <kbd>cmd</kbd>+<kbd>\\</kbd> (Mac) or <kbd>ctrl</kbd>+<kbd>\\</kbd> (Windows/Linux): change working directory (R, Julia and Python only)


- <kbd>cmd</kbd>+<kbd>b</kbd> (Mac) or <kbd>ctrl</kbd>+<kbd>b</kbd> (Windows/Linux): source current file (R, Julia and Python only)

    SendTextPlus uses Sublime build system to source files, you might have to choose the `SendTextPlus` build system before pressing the keys.

### Cmder settings

Go to `Paste` in the settings, uncheck, "Confirm <enter> keypress" and "Confirm pasting more than..."


### Some Details

- R blocks are detected by a regular expression for  `{`,`}` pairs. 
- Julia blocks are detected by `begin`, `end` pairs and indentations. 
- Python blocks are detected by indentations.
