#About

SublimeText.BlitzMax is a [Sublime Text 2][1] language definition that
provides syntax highlighting, build systems and code snippets for the [BlitzMax][2]
programming language.

##Installation

This package has been submitted to the [Package Control][3] index and will hopefully soon be
available in the main list. You can then install it via the Command Palette (CTRL + Shift + P),
typing `install` and selecting `Package Control: Install Package`. In the subsequent popup text box
type `blitzmax` and pick the `BlitzMax` package.

In the meantime, or if you do not use Package Control, download a [zip][4] or [tarball][5] archive,
extract the archive, rename the directory to `BlitzMax` and simply drop this directory into
your Sublime Text 2 Packages directory.

#NOTES

##Syntax Highlighting Limitations

In an effort to ensure that custom BlitzMax types can be highlighted correctly an assumption has
been made that type names match the following regex '[T][A-Z]\\w*'.  For example: 'TMyType', 'TAABB'
_not_ 'Tmytype', 'MyType' or 'mytype', etc.

This format is already widely used by BlitzMax developers, and is pretty much the standard in the
existing BlitzMax code base.

##Build Systems

In order for the build systems to work the 'BlitzMax/bin' directory needs to be in your system path.

There are 4 build systems included with this plugin:

	* BlitzMax - Build and Run Console
	* BlitzMax - Build and Run GUI
	* BlitzMax - Build Console
	* BlitzMax - Build GUI

Again, certain assumptions have been made with the build systems to support building with both
Sublime Projects and individual BlitzMax source files:

1. If you don't have a project open, then the build system will attempt to build the file
currently being edited.

2. If you have a project open, the build system will attempt to build a BlitzMax source file
with the same name as the project in the root directory.  This means you don't have to keep
reselecting the main entry point source file before building.  For example if you're
editing file 'PROJECT_ROOT/Include/MySourceFile.bmx' and your project file is called
'MyNewGame.sublime-project' then the build system will attempt to build
'PROJECT_ROOT/MyNewGame.bmx' rather than the currently edited file.

##Bug Reports and Feature Requests

If you find any problems with this plugin, please raise an issue at the repository's [issue tracker][6],
including a detailed description of the issue and if possible a section of example code which
highlights the issue.

Requests for new features can also be raised at the same location.

#License

SublimeText.BlitzMax is released under the MIT license.

Copyright (c) 2013 Paul Maskelyne (Muttley) <muttley@muttleyville.org>

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and
associated documentation files (the "Software"), to deal in the Software without restriction,
including without limitation the rights to use, copy, modify, merge, publish, distribute,
sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial
portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT
NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES
OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

[1]: http://www.sublimetext.com/
[2]: http://www.blitzbasic.com/Products/blitzmax.php
[3]: http://wbond.net/sublime_packages/package_control
[4]: https://bitbucket.org/muttley/sublimetext.blitzmax/get/tip.zip
[5]: https://bitbucket.org/muttley/sublimetext.blitzmax/get/tip.tar.bz2
[6]: https://bitbucket.org/muttley/sublimetext.blitzmax/issues?status=new&status=open
