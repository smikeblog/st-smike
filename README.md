# st-smike
### version 0.8.2
### tested on Manjaro 19.02 and Arch with Openbox

# Download st from suckless.org

# Make dir for patches
  mkdir patches

# Put patches in this dir. 
  1)  st-alphaFocusHighlight-20200216-26cdfeb.diff  for transparency with picom
  2)  st-scrollback-20190331-21367a0.diff           scroll capability
  2a) st-scrollback-mouse-20191024-a2c479c.diff     add mouse support to scroll
  3)  st-copyurl-20190202-3be4cf1.diff              copy url from terminal screen
  4)  st-externalpipe-0.8.2.diff                    use dmenu to open url in $BROWSER
  5)  st-font2-20190416-ba72400.diff                additional fonts 

# Patch procedure as I do

  1) patch -Np1 -i patches/st-alphaFocusHighlight-20200216-26cdfeb.diff
    note) success
  2) patch -Np1 -i st-scrollback-20190331-21367a0.diff
    note) success
  a) patch -Np1 -i st-scrollback-mouse-20191024-a2c479c.diff
    note) success
  3) patch -Np1 -i st-copyurl-20190202-3be4cf1.diff
    note) success
  4) patch -Np1 -i st-externalpipe-0.8.2.diff
    note) success
  4) patch -Np1 -i st-font2-20190416-ba72400.diff
    note) fail   need manual patching

NOTE: The dmenu url, copy url is taken from lukesmithxyz-s st-luke.git     
        - fonts used 
            mono    from original st sources
            Inconsolata for Powerline    - yay -S powerline-fonts
            Hack Nerd Font Mono          - yay -S nerd-fonts-hack
  

