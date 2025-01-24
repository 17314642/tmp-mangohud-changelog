# Blacklist
- UplayWebCore.exe
- halloy

# Fixes
- `read_cfg` didn't properly overwrite config options
- logging would sometimes crash if it returned an empty vec
- mangoapp didn't properly respond to hide/show hud

# Changes
- Multiple GPUs can be displayed
- Changed logger errors to debug
- Added CPU power to logging
- Improved wayland keybinds
- `exec` was overlapping itself in horizontal
- Added Intel GPU metrics for i915 and xe kernel drivers
- Memory usage has been refactored to be inline with other apps

# Params
- `network_color`  sets the color of the network hud element
-  `display_server` shows if the display server is Xorg, Xwayland or wayland
-  `gpu_list` set the GPUs to display in the hud e.g `gpu_list=0,1`
- `proc_mem` and `io_read` now works properly in gamescope
