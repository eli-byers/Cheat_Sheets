# Atom Hotkeys
These work on mac in Atom. This is not a complete list at all, just a small set of tools that can speed up your deveopment. [Here](https://github.com/nwinkler/atom-keyboard-shortcuts) is a more complete list of shortcuts.

###Table of Contents
* [Formating](#formating)
* [Move Cursor](#cursor)
* [Find & Select](#find--select)
* [Delete](#delete)

### Symbol Reference
| Symbol       | Decsciption             |
| ------------ | ----------------------- | 
| &#x2318;     | the Command Key			 |
| &#x2325;     | the Option Key          |
| &#x2303;     | the Control Key         |
| &#x21E7;     | the Shift Key           |
| &#x2191;     | the Up Arrow Key        |
| &#x2193;     | the Down Arrow Key      |
| &#x2190;     | the Left Arrow Key      |
| &#x2192;     | the Right Arrow Key     |


### Formating
| Command         | Key                            | Decsciption |
| --------------- | ------------------------------ | ----------- |
| Duplicate       | &#x2318; + &#x21E7; + D        |Duplicate the line the cursor is on. <br> If multiple lines are selected, duplicate all selected lines. |
| Indent          | &#x2318; + ]                   | Indent the line the cursor is on. <br> If multiple lines are selected, indent all selected lines |
| Unindent        | &#x2318; + [                   | Unindent the line the cursor is on <br> If multiple lines are selected, unindent all selected lines |
| Auto indent     | &#x2303; + &#x2318; + i        | Auto indent the selected lines. <br> This doesn't always create correct indentation, use with caution. |
| Move lines up   | &#x2303; + &#x2318; + &#x2191; | Move the line the cursor is on up one line. <br> If multiple lines are selected, move all selected lines up. |
| Mode lines down | &#x2303; + &#x2318; + &#x2193; | Move the line the cursor is on down one line. <br> If multiple lines are selected, move all selected lines down.

### Cursor 
| Command             | Key                            | Decsciption |
| ------------------- | ------------------------------ | ------------|
| Start of line       | &#x2303; + a                   | Move cursor to the beginning of the current line. |
| End of line         | &#x2303; + e                   | Move cursor to the end of the current line.
| Left one word       | &#x2325; + &#x2190;            | Move the cursor left one word.  |
| Right one word      | &#x2325; + &#x2192;            | Move the cursor right one word. |
| Starting Bracket    | &#x2303; + m                   | Go to starting bracket of current code block. <br> If at the start, go to ending bracket. |
| Multiple Cursors    | &#x2318; + click               | Get another cursor wherever you click. <br> When you type or delete it will happen at all cursors. |
| Create curser above | &#x2303; + &#x21E7; + &#x2191; | Create a cursor on the line above the cursor. |
| Create curser below | &#x2303; + &#x21E7; + &#x2193; | Create a cursor on the line below the cursor. |

### Find & Select
| Command             | Key                     | Decsciption |
| ------------------- | ----------------------- |-------------|
| Find	               | &#x2318; + f            | Opens the find dialog box |
| Select matching     | &#x2318; + d            | Select the current word the cursor is on. <br> Multiple presses selects the next matching instance of that string in the file. <br> It is a direct string comparison and will select substrings if it finds any. |
| Select all matching | &#x2303; + &#x2318; + g | Select all matching strings to the word that the cursor is currently on. |

### Delete
| Command        | Key                     | Decsciption |
| -------------- | ----------------------- |-------------|
| To end of line | &#x2303; + k            | Delete from the cursor to the end of the current line. |
| Whole line     | &#x2303; + &#x21E7; + K | Delete the whole line |

<br>
---
<center> [Home](README.md) | [Top](#atom-hotkeys) </center>

