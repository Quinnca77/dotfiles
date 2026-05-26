Every separate application has their own folder which is not part of the actual path in `$HOME`.
To create a new dotfile, simply make a directory for this application first:
```
mkdir app
```
then move the whole filepath of the app to this directory. Make sure the entire filepath from `$HOME` is copied exactly:
```
cd && mv .app_dot_file dotfiles/app
```
Of course this assumes the dotfile is at the root of `$HOME`.

Finally, stow the folder with GNU stow such that it makes a symlink at `$HOME`:
```
stow app
```
The symlink will start from the directory UNDER `app`.
