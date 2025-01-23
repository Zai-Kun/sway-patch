## Some patches for sway to add additional functionality

### Installing these patches
*Tested on v1.10 of sway and 0.18 of wlroots*

1. Clone the sway repo and cd into it: `git clone https://github.com/swaywm/sway && cd sway`
2. Clone the wlroots repo into subprojects/wlroots: `git clone https://gitlab.freedesktop.org/wlroots/wlroots.git subprojects/wlroots`
4. Clone the patches repo: `git clone https://github.com/Zai-Kun/sway-patch`
3. Switch to stable branches: `git checkout v1.10 && cd subprojects/wlroots && git checkout 0.18 && cd ../..` (Optional step but recommended for stability)
5. Apply all the patches: `patch -p1 < ./sway-patch/patches/*.patch` (If you only wish to apply a specific patch, replace the wildcard '*' with the patch name)

Alright, all the preparations have been completed; now it's time to compile:
1. Compile all the code: `meson setup --wipe build/ && ninja -C build/`

Now, you should have patched version of sway in: `./build/sway/sway`. If you don't, then something went wrong.

#### Optional step
If you want to install the compiled sway into your system, do: `sudo ninja -C build/ install`
