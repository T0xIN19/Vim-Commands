# Vim-Commands
Vim-editor


===========================================================================

Insert mode - inserting/appending text
i - insert before the cursor
I - insert at the beginning of the line
a - insert (append) after the cursor
A - insert (append) at the end of the line
o - append (open) a new line below the current line
O - append (open) a new line above the current line
ea - insert (append) at the end of the word
Ctrl + h - delete the character before the cursor during insert mode
Ctrl + w - delete word before the cursor during insert mode
Ctrl + j - begin new line during insert mode
Ctrl + t - indent (move right) line one shiftwidth during insert mode
Ctrl + d - de-indent (move left) line one shiftwidth during insert mode
Ctrl + n - insert (auto-complete) next match before the cursor during insert mode
Ctrl + p - insert (auto-complete) previous match before the cursor during insert mode
Ctrl + rx - insert the contents of register x
Ctrl + ox - Temporarily enter normal mode to issue one normal-mode command x.
Esc or Ctrl + c - exit insert mode

===================================================================================

Exiting
:w - write (save) the file, but don't exit
:w !sudo tee % - write out the current file using sudo
:wq or :x or ZZ - write (save) and quit
:q - quit (fails if there are unsaved changes)
:q! or ZQ - quit and throw away unsaved changes
:wqa - write (save) and quit on all tabs

=================================================================================

Visual commands
> - shift text right
< - shift text left
y - yank (copy) marked text
d - delete marked text
~ - switch case
u - change marked text to lowercase
U - change marked text to uppercase
Registers
:reg[isters] - show registers content
"xy - yank into register x
"xp - paste contents of register x
"+y - yank into the system clipboard register
"+p - paste from the system clipboard register

===================================================================================

Global
:h[elp] keyword - open help for keyword
:sav[eas] file - save file as
:clo[se] - close current pane
:ter[minal] - open a terminal window
K - open man page for word under the cursor


=========================================================================

Editing
r - replace a single character.
R - replace more than one character, until ESC is pressed.
J - join line below to the current one with one space in between
gJ - join line below to the current one without space in between
gwip - reflow paragraph
g~ - switch case up to motion
gu - change to lowercase up to motion
gU - change to uppercase up to motion
cc - change (replace) entire line
c$ or C - change (replace) to the end of the line
ciw - change (replace) entire word
cw or ce - change (replace) to the end of the word
s - delete character and substitute text
S - delete line and substitute text (same as cc)
xp - transpose two letters (delete and paste)
u - undo
U - restore (undo) last changed line
Ctrl + r - redo
. - repeat last command


==============================================================================

Macros
qa - record macro a
q - stop recording macro
@a - run macro a
@@ - rerun last run macro



==============================================================================


Cut and paste
yy - yank (copy) a line
2yy - yank (copy) 2 lines
yw - yank (copy) the characters of the word from the cursor position to the start of the next word
yiw - yank (copy) word under the cursor
yaw - yank (copy) word under the cursor and the space after or before it
y$ or Y - yank (copy) to end of line
p - put (paste) the clipboard after cursor
P - put (paste) before cursor
gp - put (paste) the clipboard after cursor and leave cursor after the new text
gP - put (paste) before cursor and leave cursor after the new text
dd - delete (cut) a line
2dd - delete (cut) 2 lines
dw - delete (cut) the characters of the word from the cursor position to the start of the next word
diw - delete (cut) word under the cursor
daw - delete (cut) word under the cursor and the space after or before it
:3,5d - delete lines starting from 3 to 5
Tip You can also use the following characters to specify the range:
e.g.
:.,$d - From the current line to the end of the file
:.,1d - From the current line to the beginning of the file
:10,$d - From the 10th line to the beginning of the file
:g/{pattern}/d - delete all lines containing pattern
:g!/{pattern}/d - delete all lines not containing pattern
d$ or D - delete (cut) to the end of the line
x - delete (cut) character



==============================================================================


Cursor movement
h - move cursor left
j - move cursor down
k - move cursor up
l - move cursor right
gj - move cursor down (multi-line text)
gk - move cursor up (multi-line text)
H - move to top of screen
M - move to middle of screen
L - move to bottom of screen
w - jump forwards to the start of a word
W - jump forwards to the start of a word (words can contain punctuation)
e - jump forwards to the end of a word
E - jump forwards to the end of a word (words can contain punctuation)
b - jump backwards to the start of a word
B - jump backwards to the start of a word (words can contain punctuation)
ge - jump backwards to the end of a word
gE - jump backwards to the end of a word (words can contain punctuation)
% - move to matching character (default supported pairs: '()', '{}', '[]' - use :h matchpairs in vim for more info)
0 - jump to the start of the line
^ - jump to the first non-blank character of the line
$ - jump to the end of the line
g_ - jump to the last non-blank character of the line
gg - go to the first line of the document
G - go to the last line of the document
5gg or 5G - go to line 5
gd - move to local declaration
gD - move to global declaration
fx - jump to next occurrence of character x
tx - jump to before next occurrence of character x
Fx - jump to the previous occurrence of character x
Tx - jump to after previous occurrence of character x
; - repeat previous f, t, F or T movement
, - repeat previous f, t, F or T movement, backwards
} - jump to next paragraph (or function/block, when editing code)
{ - jump to previous paragraph (or function/block, when editing code)
zz - center cursor on screen
zt - position cursor on top of the screen
zb - position cursor on bottom of the screen
Ctrl + e - move screen down one line (without moving cursor)
Ctrl + y - move screen up one line (without moving cursor)
Ctrl + b - move back one full screen
Ctrl + f - move forward one full screen
Ctrl + d - move forward 1/2 a screen
Ctrl + u - move back 1/2 a screen
Tip Prefix a cursor movement command with a number to repeat it. For example, 4j moves down 4 lines.


==============================================================================

