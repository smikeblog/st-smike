# st-smike
### version 0.8.4
### tested on Manjaro, MX and Arch with Openbox

# Download st from suckless.org

# Make dir for patches
  mkdir patches

# Put patches in this dir.
  1)  st-alpha 			            transparency with picom
    1a) Alpha Focus Highlight       specify two opacity/background colors
  2)  st-scrollback                 scroll capability
  3)  st-copyurl 		            copy url from terminal screen
  4)  st-externalpipe		        use dmenu to open url in $BROWSER
  5)  st-font2                      additional fonts

# Patch procedure as I do

  1) patch -Np1 -i patches/st-alpha-*.diff
    note) success
  1a) patch -Np1 -i patches/st-focus-*.diff
  2) patch -Np1 -i patches/st-scrollback-*.diff
    note) success
  3) patch -Np1 -i patches/st-copyurl-*.diff
    note) success
  4) patch -Np1 -i patches/st-externalpipe-*.diff
    note) success
  5) patch -Np1 -i patches/st-font2-*.diff
    note) fail   need manual patching

NOTE: The dmenu url, copy url is taken from lukesmithxyz-s st-luke.git
```
        - fonts used
            mono    from original st sources
            Inconsolata for Powerline    - yay -S powerline-fonts
            Hack Nerd Font Mono          - yay -S nerd-fonts-hack
```

