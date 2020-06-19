# st-smike
### version 0.8.3
### tested on Manjaro and Arch with Openbox

# Download st from suckless.org

# Make dir for patches
  mkdir patches

# Put patches in this dir.
  1)  st-alpha 			            transparency with picom
    1a) Alpha Focus Highlight       specify two opacity/background colors
  2)  st-scrollback                 scroll capability
  3)  st-copyurl 		            copy url from terminal screen
  4)  st-externalpipe		        use dmenu to open url in $BROWSER
    4a) st-externalpipe-eternal	    use dmenu to open url in $BROWSER
  5)  st-font2                      additional fonts

# Patch procedure as I do

  1) patch -Np1 -i patches/st-alpha-0.8.2.diff
    note) success
  2) patch -Np1 -i patches/st-scrollback-20200419-72e3f6c.diff
    note) success
  3) patch -Np1 -i patches/st-copyurl-20190202-3be4cf1.diff
    note) success
  4) patch -Np1 -i patches/st-externalpipe-0.8.2.diff
    note) success
  4a) patch -Np1 -i patches/st-externalpipe-eternal-0.8.3.diff
  5) patch -Np1 -i patches/st-font2-20190416-ba72400.diff
    note) fail   need manual patching

NOTE: The dmenu url, copy url is taken from lukesmithxyz-s st-luke.git
```
        - fonts used
            mono    from original st sources
            Inconsolata for Powerline    - yay -S powerline-fonts
            Hack Nerd Font Mono          - yay -S nerd-fonts-hack
```

