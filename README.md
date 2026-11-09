Hey, I'm Pradyumn. I build low-level systems, Linux appliances, and explore graphics engines.

Most of my time goes into experimenting with operating system plumbing: boot paths, static init supervisors, Wayland compositor internals, and immutable filesystems.

---

### Projects

* **[kurogane](https://github.com/devpryan7792/kurogane)** (`Rust`) — Static micro-supervisor (`kurogane-init`) and immutable Linux appliance engine. Packages workloads into compressed, read-only EROFS images (`lz4hc,12`) with decoupled Wayland mediation (`cage` + `seatd`) and zero-allocation pre-exec sandboxing. Boots under 1.8s in QEMU. Live portal at [is.gd/kurogane](https://is.gd/kurogane).
* **[chronodb](https://github.com/devpryan7792/chronodb)** (`Rust`) — Embedded append-only storage engine. Memory-mapped zero-copy reads, CRC32-C verified pages, crash-safe writes, and sub-microsecond point-in-time (`as-of`) entity queries.
* **[hyprquickshell](https://github.com/devpryan7792/hyprquickshell)** (`QML`, `Shell`) — Daily driver desktop setup. Arch Linux + Hyprland interface built on Quickshell and Qt6/QML, with Matugen dynamic theming and turnkey automation.
* **[kaze-os](https://github.com/devpryan7792/kaze-os)** (`Shell`) — Modular Arch Linux build engine generating specialized Wayland desktop flavors (Hayate, Kasumi, Nagomi).
* **[saknussemm](https://github.com/devpryan7792/saknussemm)** (`JavaScript`, `GLSL`) — Scroll-driven subterranean web journey honoring Jules Verne. Custom 2.5D volumetric light beams (god rays), normal-mapped rock strata, and WebGL fluid distortion shaders.
* **[impulse3d](https://github.com/devpryan7792/impulse3d)** (`TypeScript`) — Zero-dependency 3D rigid-body physics engine with an interactive Three.js playground.

---

### Upstream Contributions

Patches and bug fixes I've submitted to tools in my daily workflow:

#### Merged
* **[hyprwm/hyprlock#1091](https://github.com/hyprwm/hyprlock/pull/1091)** — Defers auth initialization until the session lock surface is acquired.
* **[hyprwm/hypridle#212](https://github.com/hyprwm/hypridle/pull/212)** — Uses generic `kbd_backlight` device in example configuration.
* **[litestar-org/advanced-alchemy#834](https://github.com/litestar-org/advanced-alchemy/pull/834)** — Classifies DuckDB integrity errors by native error type.
* **[janbjorge/pgqueuer#954](https://github.com/janbjorge/pgqueuer/pull/954)** — Driver refactor removing unused `tm` property and task manager ports.
* **[oxpull/django-ox#149](https://github.com/oxpull/django-ox/pull/149)** — Adds `ox_retry` and `ox_discard` CLI commands.

#### In Review & Ongoing
* **[python/cpython#159081](https://github.com/python/cpython/pull/159081)** — Corrects `UnicodeDecodeError` byte offsets in `utf-8-sig` when input has a BOM.
* **[CapSoftware/Cap#3534](https://github.com/CapSoftware/Cap/pull/3534)** — Resolves PipeWire system audio routing timeout on Linux.
* **[litestar-org/advanced-alchemy#833](https://github.com/litestar-org/advanced-alchemy/pull/833)** — Prevents filter dependency collisions in merged service bundles.
* **[simonw/sqlite-utils#917](https://github.com/simonw/sqlite-utils/pull/917)** — Migrates deprecated `CliRunner.isolated_filesystem` to `tmp_path`.
* Other explorations in `hyprwm/Hyprland`, `astral-sh/ruff`, and `psycopg`.

---

<details>
  <summary>Environment</summary>
  <br>

  - **OS**: Arch Linux
  - **Compositor**: Hyprland
  - **Terminal**: Ghostty
  - **Languages**: Rust, C/C++, TypeScript, Python, Shell
  - **Virtualization & Testing**: QEMU / KVM
</details>
