# Python on Windows

## Installation

1. Download and run the Windows Python installer from
   https://www.python.org/downloads.

2. Click "Install now" and wait until installation completes.

3. Start a command prompt. Winkey | cmd<enter>

4. Start Python, verifying installation.

   ```
   C:\Users\hitbox>py
   >>>
   ```

The Windows Python installer puts a binary called `py` in the Windows
installation directory. Which is why you don't need the Python executable on
your PATH (an option in the installer).

## virtualenv

1. Create a virtual environment.

   In cmd.exe

   ```
   C:\Users\hitbox\project>py -m venv venv
   ```

2. Activate it.

   ```
   C:\Users\hitbox\project>venv\Scripts\activate.bat
   (venv) C:\Users\hitbox\project>
   ```

## Package Manager

1. Use pip to manage Python modules

   Globally

   ```
   C:\Users\hitbox>py -m pip install ...
   ```

   In a virtual environment

   ```
   C:\Users\hitbox\project>venv\Scripts\activate.bat
   (venv) C:\Users\hitbox\project>py -m pip install ...
   ```

## Recommendations

1. Git for Windows

   Provides git and a Linux-like (bash) environment for Windows.

   https://git-scm.com/download/win (automatic download)

   Git for Windows comes with vim.

   Somewhat supports tabs--when you have multiple Git windows open, you can
   Ctrl+Tab between them.

   You will have to prepend `winpty` to many Windows executables to run them
   inside Git for Windows.

   ```
   $ winpty py
   >>>
   ```

   If you don't, you'll have to kill the process and add `winpty`.

   I create aliases in .bashrc

   ```
   alias python='winpty python'
   ```

   Other programs, like `psql`, need `winpty` too.

2. neovim

   An extension of vim with a Windows GUI binary. There's gvim but neovim
   performs better for me, on my weaker laptop. It doesn't have an installer
   however, so where you put it and how you run it is up to you.

3. clink

   https://mridgers.github.io/clink/

   Readline goodies for when you have to be in cmd.exe.

4. dotfiles

   Keep your config files in a bare git repo.

   https://developer.atlassian.com/blog/2016/02/best-way-to-store-dotfiles-git-bare-repo/
