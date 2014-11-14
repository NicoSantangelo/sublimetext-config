SublimeText-Config **WIP**
==================

Packages, keybindings and settings from my Sublime Text configuration.


# Keybindings

Platforms

## Vintage

The Vintage config is mostly done to try to merge SublimeText shortcuts without leaving the confort of the home row.

### Useful bindings

````json
    //
    // Overlay (use GoTo Anything panel without using the arrow keys):

    // Move right in overlay (open tab)
    { "keys": ["super+l"], "command": "move", "args": { "by": "characters", "forward": true },
        "context": [ { "key": "overlay_visible", "operator": "equal", "operand": true } ]
    },

    // Move down in overlay
    { "keys": ["super+j"], "command": "move", "args": { "by": "lines", "forward": true },
        "context": [ { "key": "overlay_visible", "operator": "equal", "operand": true } ]
    },

    // Move up in overlay
    { "keys": ["super+k"], "command": "move", "args": { "by": "lines", "forward": false },
        "context": [ { "key": "overlay_visible", "operator": "equal", "operand": true } ]
    },

    //
    // Move in search results and go to definition

    { "keys": ["g", "o"], "command": "next_result", "context": [{ "key": "setting.command_mode" }] },
    { "keys": ["g", "O"], "command": "prev_result", "context": [{ "key": "setting.command_mode" }] },

    { "keys": ["g", "d"], "command": "goto_definition", "context": [{ "key": "setting.command_mode" }] },

    //
    // Multiple cursors and moving lines

    // Multiselection (more than one cursor)
    { "keys": ["super+alt+k"], "command": "select_lines", "args": {"forward": false}, "context": [{"key": "setting.command_mode"}] },
    { "keys": ["super+alt+j"], "command": "select_lines", "args": {"forward": true}, "context": [{"key": "setting.command_mode"}] },
    
    // Move lines
    { "keys": ["super+shift+k"], "command": "swap_line_up", "context": [{"key": "setting.command_mode"}] },
    { "keys": ["super+shift+j"], "command": "swap_line_down", "context": [{"key": "setting.command_mode"}] },
````

# Packages

I have the following packages installed:

````
AAAPackageDev                  RubyTest
All Autocomplete               Sass
ApplySyntax                    SublimeERB
Better Completion              SublimeGit
EasyMotion                     SublimeLinter
Emmet                          SublimeLinter-jshint
File Navigator                 SublimeLinter-pylint
GitGutter                      SublimeLinter-ruby
Gulp                           SublimeREPL
I18n Rails                     Sublimerge Pro
Jasmine                        Surround
Monokai Extended               Terminal
MoveTab                        Theme - Gravity
Origami                        Theme - Spacegray
PlainTasks                     Trello
Predawn                        Vintage Escape
Quick File Creator             Vintage Surround
Rails Partial                  Vintage-Origami
RSpec (snippets and syntax)    
````

if you're using [Package Control](https://sublime.wbond.net/), you can add any of those names to your `Package Control.sublime-settings` file and after restaring it will be installed automatically

## Package Control

Install stuff

# Preferences

The preferences file it's probably a personal thing, but a few interesting options are:

````json
{
    //
    // Exclude patterns so you get cleaner searches
    "file_exclude_patterns": [ /*...*/ ],
    "folder_exclude_patterns": [ /*...*/ ],

    //
    // To use along side origami, to have the split on focus take up 75% of the screen
    "origami_auto_zoom_on_focus": 0.75

    //
    // Vim
    // Have a block caret and start in command mode
    "highlight_line": false,
    "inverse_caret_state": true,
    "caret_style": "phase",
    "vintage_start_in_command_mode": true,
}
````
