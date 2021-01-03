# Windows Setup

1. Update your computer to at least Windows 10, version 2004. (Version 1903 may work but 2004 is ideal.)

   - Use `winver` to check the current version.
   - https://en.wikipedia.org/wiki/Windows_10_version_history

2. Install [Windows Subsystem for Linux (WSL 1)](https://docs.microsoft.com/en-us/windows/wsl/install-win10#manual-installation-steps).

3. Restart.

4. Install [Ubuntu](https://www.microsoft.com/store/apps/9nblggh4msv6) from Windows Store.

   - Setup user/pass.
   - Create shortcut to WSL home folder on desktop.

5. Install [Windows Terminal](https://aka.ms/terminal).

   - Pin Windows Terminal to taskbar.
   - Change `defaultProfile` and set `"startingDirectory":"\\\\wsl$\\[DISTRONAME]\\home\\[USERNAME]"`.

6. Install Sublime Text 3.

   - Disable Hot Exit.

7. Install [wsl-open](https://github.com/4U6U57/wsl-open).

   ```
   # Make a bin folder in your home directory
   mkdir ~/bin

   # Add the bin folder to your PATH in your bashrc
   echo '[[ -e ~/bin ]] && PATH=$PATH:~/bin' >> .bashrc

   # Download the script to a file named 'wsl-open'
   curl -o ~/bin/open https://raw.githubusercontent.com/4U6U57/wsl-open/master/wsl-open.sh

   # Mark file as safe to run
   chmod +x ~/bin/open
   ```

8. Install [`wsl-subl`](https://github.com/AlJohri/wsl-subl).

   ```
   # Download the script to a file named 'wsl-subl'
   curl -o ~/bin/subl https://raw.githubusercontent.com/AlJohri/wsl-subl/master/wsl-subl.sh

   # Mark file as safe to run
   chmod +x ~/bin/subl
   ```