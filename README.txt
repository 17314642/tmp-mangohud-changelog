Currently 33% is done, scroll below to find where I stopped.

### Changes:
+ e6b7304 [blacklist] Add Ubisoft store
+ 193fdc7 logging: add cpu power
+ d102604 fpsmetrics: refactor FPS calculation in metrics

### Fixes:
+ 2937785 params: fix read_cfg not overriding config options
+ ed6cf22 present_mode: proper vsync implementation
+ 2d0c0a1 doc: add network_color to README and MangoHud.conf
+ 159eb13 wayland: Fix some issues with wayland keybinds
+ c0afb84 shell: edit the command if steam runtime
+ 4933695 build deps: arch: add 32bit xkbcommon
+ a6422bc Build.sh: add missing deps for suse
+ 2e7e86f vulkan: Fix present mode fallback override
+ 8b7dae6 Fix compilation without wayland

### Parameters:
+ 7cfca3f param: display_server

### All commits from 0.7.2:

- `-` - should not be mentioned
- `+` - should be mentioned


- b217d75 meson.build - v0.7.2
+ e6b7304 [blacklist] Add Ubisoft store
- 391c522 Update blacklist.cpp
- 511b7a6 Shell: add debug for cmd and output
- a4393e0 Shell: read: only get last line
- 4307450 params: control: change errors to debug
- 4a34502 Add virtual dtor to CPUPowerData
- eaa96ec shell: attempt to fix showing ld error
+ 2937785 params: fix read_cfg not overriding config options
- 41f2cf7 shell: just unset LD_PRELOAD on all commands


- f8fb9aa shell: unset LD_PRELOAD at init
- 89a6f01 workflow: update mangohud version
- 41b8761 Fix reference URL
- 9cb5a40 mangoapp: fix deviceID for nvidia GPUs
- 2b00432 mingw: let meson set link args
- 9955b22 readme: gamescope note
- 392f18d xnvctrl: change error to debug
+ 193fdc7 logging: add cpu power
- df61c66 logging: return on empty vec
- 2a2cc4a Update MangoHud.conf


+ ed6cf22 present_mode: proper vsync implementation
+ 2d0c0a1 doc: add network_color to README and MangoHud.conf
- 8a31b96 cpu: temp: don't break on asusec if missing node
- 6c66565 mangoplot: look for header further down than 4 rows
+ 159eb13 wayland: Fix some issues with wayland keybinds
+ c0afb84 shell: edit the command if steam runtime
- edf7546 mangoapp: fix comparison warning
- bda2af4 fps_metrics: fix incorrect iteration
- 8f94973 exec: use prev ret if bad system call
- c0b609f mangoapp: Use XInitThreads


- 1abf530 Update issue templates
+ 7cfca3f param: display_server
- 422663d params: display_server: fix mingw build
+ 4933695 build deps: arch: add 32bit xkbcommon
- e248ee9 display_server: capitalize in hud
- 6c74e3c deps: fix typo in arch deps
- b585329 readme: fix typo
- 7fafed9 rework fps_metrics for all cases
- e8817f8 doc: add present_mode to MangoHud.conf
- 606fa27 use egl to get wayland display


- 1696a55 fix egl x11 crashes
- 1d47ed8 init to null
- 3c58162 chore: fix typos
+ a6422bc Build.sh: add missing deps for suse
+ d102604 fpsmetrics: refactor FPS calculation in metrics
- d0894ff elfhacks: d_un.d_ptr is relative on riscv glibc
- 4b45e26 elfhacks: d_un.d_ptr is relative on mips glibc too
+ 2e7e86f vulkan: Fix present mode fallback override
+ 8b7dae6 Fix compilation without wayland
- feef6e3 Include map header in hud_elements.h


=====================================================================================================
FINISHED HERE (33% done)
=====================================================================================================


+ d224507 Rework GPUs to allow for multiple
- 0981acf Meson: revert to c++14
+ 237816f params: gpu_text changed to a list
+ b58811b horizontal: fix gpu and vram displaying incorrectly
- 53ead5a mingw: gpu: fix filesystem error
- 9c9ad09 gpu: fix dangling pointer
- 77b3f36 update regex in the get_pci_device_address method to also match addresses with characters
+ 3bf75d1 Output mangohud version in debug logs
- 9103869 gpu: set false to is_active so we don't end up with multiple active ones
+ ba35a61 Fixed cpu temp not getting updated


+ c8cfeb4 gpu: catch stoul exceptions
- 2732de1 gpus: fix init vid and pid
+ 99c8855 wayland: Fix crash in multi-seat sessions
- 7b2dea5 fix gpu_text vector bounds checking
- e77ff17 nvctrl: use find_nv_x11 dpy instead
- c29db43 xnvctrl: fix display variable
+ d5430fa nvml: don't look for compute but graphics instead
+ 55bd152 gpu: look for render instead of card
+ e422dc8 param: gpu_list
+ 477001c Fix find_nv_x11 logging


+ d871c3e fix mangoapp hide/show
- 71d2fa9 nvidia: remove unnecessary include xlib
- 024cf21 gpu: fix gpu_name for single GPU
- 29898db nvidia: check that logger isn't null before accessing
- bef3a29 amdgpu: remove DETECT_OS_UNIX directive
- 55d8466 meson: add deps to amdgpu test
+ f6eee93 add intel gpu usage support via fdinfo and fix fdinfo code a little
- 452ce76 use ifdef __linux__ instead of DETECT_OS_UNIX
+ 560484a blacklist: add halloy
+ 4347b31 horizontal layout: fix exec overlapping


+ d8dbe68 logging: fix double-logging of avg fps
+ 5172caa param: do update_fan() only when fan=1
- 2153f81 mingw: cpu: add dummy read temp file func
+ 1d19d43 gpu: text: single GPUs should just be named GPU, no index
- 4ab106f readme: detail meson options
- 744c188 Fix potential undefined behavior in params initialization for C++14 compliance
+ 258491e nvidia: fix faulty nvml check
+ 66195f4 nvidia: only try to get metrics if module is available
- b12b698 nvml: remove redundant line
+ e8a51ae nvml: add missing nvml available check


+ c8a08b9 nvidia: don't try to get pids if nvml is not available
- a109f0b gpu: if no active gpu is set, assume first one
+ 8bd0b63 Nuke mangoapp layer
+ 3b0a0d4 mangoapp layer: more nukes
+ afaa7d1 Fix network for horizontal bar
+ 4247170 gpu_fdinfo: add vram usage
+ 816b4de gpu_fdinfo: add power usage for intel gpu via hwmon
- 55a1340 gpu_fdinfo: check if hwmon exists
- 3320601 gpu_fdinfo: limit stats gathering to every 500ms
- 24daceb gpu_fdinfo: use sleep instead of time comparison


- d9e312f gpu_fdinfo: fix power usage calculation
- 26c0f0a gpu_fdinfo: replace c code with c++ and minor fixes
- 1cad9c8 gpu_fdinfo: move find_fd() to the right place
- 22c7523 gpu_fdinfo: fix formatting
- 6c49103 gpu_fdinfo: determine if i915 or xe driver is used
- af0d80c gpu_fdinfo: divide logic in separate sections
+ ae4c411 gpu_fdinfo: add support for intel xe driver
- 975815c gpu_fdinfo: remove duplicate fdinfo enumeration
- eca6a30 README: Add missing params and info to README
- 24d3cd9 Mangohud.conf: Add missing options to conf file


- cf6c537 ubuntu workflow: fixed active_gpu_found not used
- 0e91e79 net: catch stoll for read_line of tx/rx
- b1b4a09 gpu_fdinfo: stop using static variables
- bc29131 gpu_fdinfo: rework find_fd()
+ 70bd73b gpu_fdinfo: add support for integrated intel gpus
- 1aa98dd gpu_fdinfo: fix abnormally high power usage value at first launch
- c392b72 gpu_fdinfo: calculate xe fd load separately
- 2cd355f overlay: change default spdlog level to info
+ bfc5adb gpu_fdinfo: add gpu clock support for i915 and xe
- b4c2119 gpu_fdinfo: add driver-agnostic hwmon support


- 5687c44 hud_elements: now intel cards can display fan speed too
+ fb7a0eb gpu_fdinfo: read GPU throttling status on Xe/i915 and fix formatting
- b489503 gpu: nuke find_active_gpu for unreliability
+ 81a2ad8 gpu: display all gpus by default and let user pick active gpu
+ 7a88186 NVIDIA: info if nvml and nvctrl fails
+ e8f8406 nvidia: fix vram usage metric not updating
+ 2e4069c don't rely on libx11 for keyboard shortcut loading
+ ec40c5b only enable glx with have_x11
+ 64f12d3 without x11 compile fixes
- 8007928 Fix potential crash with eglGetDisplay


- 3e456fe remove vendorID param from check_keybinds
+ c22ced0 opengl-shim
- 9556404 improve the shim
+ 5559616 support multiple lib paths (for 32 bit)
- c515999 GL: change spdlog gl version to debug
- 5ffc524 bring back old pci_dev config format
- 9dfbcf9 Move dlsym code to shim
- b447db5 Bring back --dlsym flag
- 14a6c6e Fix shim fallback code
+ 46c2ea1 gpu_fdinfo: add gamescope support


+ 921e6de gpu_fdinfo: add i915 integrated gpu support
+ 5e1cbdd gpu_fdinfo: find_fd() every 10 secs instead of once
- 4973296 fix tests compile error
- 215b362 use macros for shim
- 625a42a refactor memory.cpp
+ 0575c8e add gamescope support for proc_mem and io_read/write
+ 26164d1 [blacklist] Add Plutonium launcher
