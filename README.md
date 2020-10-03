# st-smike
### version 0.8.4
### tested on Manjaro, MX and Arch with Openbox

## features using dmenu

+ **follow urls** by pressing `alt-m`
+ **copy urls** in the same way with `alt-y`
+ **paste copied urls** with `alt-v` or `shift-insert`
+ **copy urls** with `alt-b`
+ **visualize screen in neovim with `alt-escape`

## Bindings for

+ **scrollback** with `alt-↑/↓` or `alt-k/j`or `alt-pageup/down`
+ **zoom/change font size**: `alt-l/h` or `alt-shift-pageup/down` . `alt-shift-home` or `alt-home ` returns to default
+ **copy text** with `alt-c`, **paste** is `alt-v` or `shift-insert`

## Pretty stuff

+ Default dracula colors.
+ Transparency/alpha.
+ Default font is system "mono" at 12pt, meaning the font will match your system font.


# INSTALL

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

NOTE: The dmenu url, copy url are from https://github.com/GasparVardanyan/st/blob/master/config.h#L186
```
        - fonts used
            mono    from original st sources
            Inconsolata for Powerline    - yay -S powerline-fonts
            Hack Nerd Font Mono          - yay -S nerd-fonts-hack
```

