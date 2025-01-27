# Blacklist
- Ubisoft Store (UplayWebCore.exe)
- halloy (IRC client)
- Plutonium Launcher (plutonium.exe, plutonium-launcher-win32.exe)

# Fixes
- `read_cfg` didn't properly overwrite config options
- logging would sometimes crash if it returned an empty vec
- fix double-logging of avg fps
- nvidia: warn if both nvml and xnvctrl are unavailable
- mangoapp didn't properly respond to hide/show hud
- add 32bit xkbcommon to project dependencies
- add missing dependencies for opensuse
- proper vsync implementation
- refactor FPS calculation in metrics
- fix exec, network, gpu and vram displaying incorrectly in horizontal mode

# Changes
- Multiple GPUs can be displayed
- Changed logger errors to debug
- Added CPU power to logging
- Improved wayland keybinds
- Memory usage has been refactored to be inline with other apps
- mangoapp vulkan layer is deleted (it was a testing project and no longer in development)

- If using `exec` and inside steam runtime, launch command using `steam-runtime-launch-client`
  - If mangohud is used inside flatpak, you need to allow your app to speak on `org.freedesktop.Flatpak` dbus address.
    Example if you're using mangohud in steam: `flatpak override --user --talk-name=org.freedesktop.Flatpak com.valvesoftware.Steam`

- Added Intel GPUs support (integrated and discrete, i915 and xe drivers)
  - Temperature is only available in linux 6.13+
  - Temperature and Power Usage is not available for integrated gpus
  - VRAM and GPU Usage is per-process not per-system (that would require root rights)

- Multiple GPUs support:
    - By default, MangoHud displays all GPUs. To select needed GPUs, you can use `gpu_list` or `pci_dev`

# Params
- `network_color`  sets the color of the network hud element
- `display_server` shows if the display server is Xorg, Xwayland or wayland
- `gpu_list` set the GPUs to display in the hud e.g `gpu_list=0,1`
- `proc_mem` and `io_read` now works properly in gamescope (mangoapp)
