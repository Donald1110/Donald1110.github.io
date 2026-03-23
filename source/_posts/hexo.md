---
title: Hexo Installation
date: 1969-10-29 00:00:00
category: guides
aside: true
copyright: false
archives: false
tags:
---
# Hexo!
Hexo is a powerful blog framework powered by Node.js.

To get started, an installation of the aforementioned Node.js and the npm (Node Package Manager) command interface is required.

First off, visit https://nodejs.org/en/download and download their prebuilt Node.js installers. Make sure you select the correct architecture your device is running (e.g. ARM64 for Apple Silicon Macs). The npm command interface is also installed alongside Node.js.

Both the installers and binaries work; they operate in different ways though. The .pkg (package) installers are recommended, because they are easier to use. However, if you do choose to use the binary, navigate to ./bin and run the Unix executable file.

Run `node -v` and `npm -v` in Terminal for MacOS, Command Line Interface for Windows, and the Linux Command Line for Linux.

If the terminal outputs something like:

`v24.14.0`
and 
`11.9.0`

Then Node.js and npm have been successfully installed on your device.

## Troubleshooting

If you encounter errors during installation or if `node -v` or `npm -v` returns something that differs from the examples above, according to whatever is returned, try the solutions:

### `node -v` or `npm -v` returns unexpected results

Reinstalling Node.js and npm with nvm

<i>For MacOS and Linux</i>

Installing nvm:
`curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.4/install.sh | bash`

Either restart the shell or run:
`\. "$HOME/.nvm/nvm.sh"`

Download and Install Node.js:
`nvm install 24`

Then run the previous checks again.

<i>For Windows</i>

Download and Install Chocolatey as nvm is not supported on Windows
`powershell -c "irm https://community.chocolatey.org/install.ps1|iex"`

Install Node.js
`choco install nodejs --version="24.14.0"`

Then run the previous checks again.

### EACCES or Permission Denied

Either try the same solution above or change the directory of the installation manually.

<i>For MacOS and Linux</i>

Pick and create a directory in a location:
`mkdir ~/.npm-global` or any folder name you want (e.g. `~/.npm-install`). Remember to add a dot before the folder name to make it a hidden directory.

Make npm install in that directory:
`npm config set prefix '~/.npm-global'`

Add it to PATH:
Edit your shell config (should be `~/.bashrc`, `~/.zshrc`, or `~/.profile`). The configuration file depends on the shell you are using. Check the shell by running `echo $0`. If it returns `-zsh`, then your configuration file should be `~/.zshrc` and so on.

Navigate to a folder or item using the "Go To Folder" option with ⇧⌘G (or Cmd+Shift+G) while in a Finder window. 

Add the below line in the configuration file:
`export PATH="$HOME/.npm-global/bin:$PATH`

Reload the shell:
`source ~/.zshrc` or `source ~/.bashrc` or `source ~/.profile` depending on the shell.

<i>For Windows</i>

Create a folder:
`C:\Users\YourName\npm-global`

Make npm install in that directory:
`npm config set prefix "C:\Users\YourName\npm-global"`

Add the below line in in PATH in the Environment Variables (search it up on the search bar):
`C:\Users\YourName\npm-global`

Installing npm

Run to install:
`npm install -g npm`

Then check the directory it is installed in
`which npm   # macOS/Linux`
`where npm   # Windows`

### Errors during npm install (compiling)

Download the respective tools for each OS:
- The Visual Studio Build Tools for Windows (which can be found here: https://visualstudio.microsoft.com/downloads/). Be sure to download the Build Tools. While the Visual Studio IDE works, it takes up a large amount of space and is useless if you don't develop and code much.
- The XCode Command Line Tools for MacOS (`xcode-select --install`)
- `build-essential` for Linux (`sudo apt install build-essential`)

Then try installing again.

### Other errors

The most common errors have been talked about here; if you encounter any other errors, consult this official document: https://docs.npmjs.com/common-errors

<!-- Requires more work -->

## Git

Git is another requirement for installing Hexo.

<i>For MacOS</i>

Homebrew:
`brew install git`

MacPorts:
`sudo port install git`

Xcode Command Line Tools:
Installed alongside the Command Line Tools.

<i>For Windows</i>
Use the installer provided on https://git-scm.com/install/windows

<i>For Linux</i>
Too many to list. Check https://git-scm.com/install/linux depending on your distribution.

## Installing Hexo

With npm installed, you are now ready to install Hexo:
`npm install -g hexo-cli`.

## Using Hexo

For a new folder:
`npx hexo init <folder>`
`cd <folder>`
`npm install`

<<folder>folder> represents the directory of the folder you want to use to hold all the contents of your static webpage. Dragging the folder into the shell will automatically input the directory. 

In this case, the folder you use already has Hexo initialized; you do not need to run the first and third commands.

Just run the second one so the shell can recognize where you want to work in.