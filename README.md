# Fixes for MBP 14,1 issues on linux

- See [this](https://github.com/Prn-Ice/mbp-2016-linux) repo to get started.

- Also checkout:

  - [This](https://gist.github.com/Prn-Ice/ff4d25780bfad6806630fdade84f89f0) gist.

- To fix bluetooth use [this](https://github.com/Prn-Ice/macbook12-bluetooth-driver).

- To fix audio use [this](https://github.com/Prn-Ice/snd_hda_macbookpro_fix).

- To fix keyboard and touch-pad, use [this](https://github.com/Prn-Ice/macbook12-spi-driver_fix), following instructions [here](https://gist.github.com/Prn-Ice/ff4d25780bfad6806630fdade84f89f0#keyboardtouchpadtouchbar). `local-overrides.quirks` is included in this repository.

- To fix wake from sleep

  - copy `fix_sleep.service` to `/etc/systemd/system/fix_sleep.service`.
  
  - copy `fixsleep` to `/sbin/fixsleep`.

  - make `/sbin/fixsleep` executable.

  - enable and start `fix_sleep.service`.

- For better battery

  - See [this](https://wiki.archlinux.org/title/Mac#Power_management) to start.

  - add `acpi_osi=!Darwin` to kernel boot options.

  - copy `off_thunderbolt.service` to `/etc/systemd/system/off_thunderbolt.service`.

  - copy `offthunderbolt` to `/sbin/offthunderbolt`.

  - make `/sbin/offthunderbolt` executable.

  - enable and start `off_thunderbolt.service`.
