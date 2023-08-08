## Links:
https://gitlab.ezracelli.dev/ezra/davinci-resolve.nix

## Broken on Nixos intel-ocl
### Clues
```
Hey guys I managed to fix the issue using this:

according to aur DVR requires tbb which was recently updated to onetbb bringing with it a bunch of other packages. so here's the plan

if you don't have intel skip the 1st step

    Run sudo pacman -Rc intel-oneapi-tbb and if pacman wants to remove something else other than intel-opeapi-* then downgrade those packages first and re-run the command to remove all the new stuff (eg. i had blender)


$ sudo downgrade blender
loading packages...
warning: downgrading package blender (17:3.4.1-23 => 17:3.4.1-14)

2. Install an older version of tbb from AUR: yay -S tbb2020

3. Reboot and enjoy

Source - https://www.reddit.com/r/davinciresolve … t/jd3hlm3/
```
[source](https://bbs.archlinux.org/viewtopic.php?pid=2092462#p2092462)
