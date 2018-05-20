# Configure Other Computers for Sync

Stolen from <https://adamdehaven.com/blog/how-to-sync-sublime-text-packages-and-settings-across-multiple-computers-with-dropbox/>.

## If a secondary computer is a Mac
  0. Clone this repo to `~/repos/sublimation`
  1. Close down Sublime Text
  2. Open Terminal and input the following commands

      ```shell
      # Navigate to the Sublime Text 3 Package directory.
      cd ~/Library/Application\ Support/Sublime\ Text\ 3/Packages/

      # Delete the User folder within this directory.
      rm -r User

      # Create a symlink within the Sublime Text 3 Package directory pointing to the User folder within this repo.
      ln -s ~/repos/sublimation/User
      ```

## If a secondary computer is running Windows
  0. Clone this repo to `%userprofile%\repos\sublimation`
  1. Close down Sublime Text
  2. Open Terminal and input the following commands

      ```shell
      # Navigate to the Sublime Text 3 Package directory.
      cd "%appdata%\Sublime Text 3\Packages"

      # Delete the User folder within this directory.
      rmdir -recurse User

      # Create a symlink within the Sublime Text 3 Package directory pointing to the User folder within this repo.
      cmd /c mklink /D User "%userprofile%\repos\sublimation\User"
      ```
