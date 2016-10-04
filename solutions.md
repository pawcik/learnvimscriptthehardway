# 04

* Set up a mapping so that you can press `<c-u>` to convert the current word to uppercase when you're in insert mode. 

```
imap <c-u> <esc>lmwgUiw`wi
```
    <esc> - exit insert mode
    l - <esc> moves back on char, so restore old position
    mw - mark current position
    gU{motion} - make text upper case
    iw - motion to select word
    \`w - jump to saved mark
    i - go back to insert mode

* Set up a mapping so that you can uppercase the current word with `<c-u>` when in *normal* mode.

```
nmap <c-u> mwgUiw`w
```
    mw - mark current position
    gU{motion} - make text upper case
    iw - motion to select word
    \`w - jump to saved mark
