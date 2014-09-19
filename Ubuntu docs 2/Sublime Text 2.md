Sublime
=======

There are three resources for documentation on Sublime Text 2:
- [Sublime Text 2 documentation][doc1]
- [Sublime Text Unofficial Documentation][doc2]
- [Perfect Workflow in Sublime Text 2][doc3] is a video course with tutorials covering many aspects of Sublime Text 2. Definitely nerd out over this video.

[doc1]: http://www.sublimetext.com/docs/2/
[doc2]: http://docs.sublimetext.info/en/latest/index.html
[doc3]: https://tutsplus.com/course/improve-workflow-in-sublime-text-2/

[Package Control][1]
---------------

A full-featured package manager that helps discovering, installing, updating and removing packages for Sublime Text 2.

[1]: https://sublime.wbond.net/installation

Installation is through the Sublime Text 2 console. This is accessed in Sublime via the `` ctrl+` `` shortcut. Once open, paste the following command into the console:

```python
import urllib2,os; pf='Package Control.sublime-package'; ipp = sublime.installed_packages_path(); os.makedirs( ipp ) if not os.path.exists(ipp) else None; urllib2.install_opener( urllib2.build_opener( urllib2.ProxyHandler( ))); open( os.path.join( ipp, pf), 'wb' ).write( urllib2.urlopen( 'http://sublime.wbond.net/' +pf.replace( ' ','%20' )).read()); print( 'Please restart Sublime Text to finish installation')
```

Hit `Enter` then restart Sublime for the changes to take affect.

The Command Palette
-------------------
Use `command+Shift+P` to bring up the Command Palette.  From there type `Install` to search for the `Package Control: Install` command then press `Enter`.
This will list available packages to install.  Just type in a package name to find it and hit Enter to install.

Here are some good packages to start out with:

- **SideBarEnhancements**  Adds additional commands(reveal, duplicate, new file etc) to the context menu in the sidebar.

- **Sublime Linter**  Highlights lines of code with potential errors

- **dotfiles-syntax-highlighting-st2**  Syntax Highlighting for dot files.
- **Gist**  Create and edit gists

[Creating a Symlink][2]
------------------

[2]: https://gist.github.com/artero/1236170

Sublime Text 2 includes a command line tool, `subl`, to work with files on the command line. This can be used to open files and projects in Sublime Text 2, as well working as an EDITOR for unix tools, such as git and subversion.

From the terminal enter the following:

```bash
$ ln -s /Applications/Sublime\ Text\ 2.app/Contents/SharedSupport/bin/subl /usr/local/bin/subl
```

Now we can use `subl .` (to open the entire current directory) or `sublime filename` to open a file.

Sublime Preferences
-------------------
`command+,` will open Sublime User Preferences.  User Preferences are defined in [JSON][3]. You can override system settings here.  Check `Preferences > Settings - Default` for a full list.  Here are some suggested User Preferences.

```js
{
  "color_scheme": "Packages/Color Scheme - Default/Solarized (Dark).tmTheme",
  "highlight_line": true,
  "highlight_modified_tabs": true,
  "translate_tabs_to_spaces": true,
  "trim_trailing_white_space_on_save": true,
  "highlight_active_indent_guide": true,
  "tab_size": 2,
  "font_face": "Monaco",
  "font_size": 13,
  "caret_style": "phase",
  "default_line_ending": "LF",
  "detect_indentation": true
}
```

[3]: http://en.wikipedia.org/wiki/JSON

Additional Preferences
-----

It's best to work with mono spaced fonts. [Adobe's Source Code Pro][4] is a good one you can download from [Source Forge][5].

To install, first open Font Book on your Mac.  Then unzip the Source Code Pro file and locate the OTF folder inside. Drag the OTF folder into Font Book.

To set as the default font in Sublime just add `"font_face": "SourceCodePro-Regular"` to your User Preferences.

[4]: http://blogs.adobe.com/typblography/2012/09/source-code-pro.html
[5]: http://sourceforge.net/projects/sourcecodepro.adobe/

You can also update Sublime's theme fot be more 'mac' like with the [Soda Theme][6]  Install via the package manager.  Then just add `"theme": "Soda Light.sublime-theme",` to your User Preferences.


[6]: http://buymeasoda.github.io/soda-theme/
