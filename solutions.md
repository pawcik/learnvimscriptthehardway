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

# 08 Abbreviations
# 09 More Abbreviations

```
:noremap <leader>' viw<esc>a'<esc>bi'<esc>el
```


* Try using `vnoremap` to add a mapping that will wrap whatever text you have *visually selected* in quotes.

```
:vnoremap <leader>" <esc>`<i"<esc>`>la"<esc>
```
    \`< - jump to the first character of last selection
    \`> - jump to the last character of last selection
    l - move extra left cause inserted new char
    a - insert mode after currect selection

* Map `H` in normal mode to go to the beginning of the current line.
    ```
    :noremap H 0
    ```

* Map `L` in normal mode to go to the end of the current line.
    ```
    :noremap L $
    ```
