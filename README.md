### Hi, I'm Pradyumn (`@devpryan7792`)

```text
  ┌────────────────────────────────────────────────────────────────────────┐
  │  SYSTEM : x86_64 / Linux 6.x                                           │
  │  STACK  : Rust · Wayland / Hyprland · EROFS · QEMU / KVM · TypeScript  │
  │  STATUS : Tinkering with kernel-userspace boundaries & micro-runtimes  │
  └────────────────────────────────────────────────────────────────────────┘
```

I spend most of my time tinkering with operating system plumbing, trying to understand how things work under the hood when you strip away bloated layers: bootloaders, init systems, Wayland compositors, and immutable filesystems. 

No corporate fluff, no fake 10x claims — just a curious builder reading kernel docs, writing small micro-supervisors, and breaking/fixing Linux environments under QEMU.

---

### 🛠️ What I'm Building & Tinkering With

```
  ┌─────────────────┐       ┌─────────────────┐       ┌─────────────────┐
  │   kurogane-init │ ----> │  Wayland / cage │ ----> │ immutable root  │
  │   (static Rust) │       │ (seatd mediate) │       │ (lz4hc12 EROFS) │
  └─────────────────┘       └─────────────────┘       └─────────────────┘
           │                         │                         │
           └─────────────────── sub-1.8s cold boot ────────────┘
```

* **[Kurogane (黒鉄)](https://github.com/devpryan7792/kurogane)** — An experimental Linux appliance engine and static micro-supervisor (`kurogane-init`) written in Rust. Compiles workloads into read-only EROFS images with zero-allocation pre-exec sandboxing, decoupled Wayland mediation (`cage` + `seatd`), and cold boots in under 1.8 seconds in QEMU.
  * 🌐 **Interactive Portal**: [is.gd/kurogane](https://is.gd/kurogane)
  * *Active trade-off*: Prioritizing extreme boot speed and immutability over general-purpose package management.

* **[ChronoDB](https://github.com/devpryan7792/chronodb)** — An embedded append-only time-travel storage engine in Rust.
  * Explores 4 KiB CRC32-C verified pages, memory-mapped (`mmap`) zero-copy reads, and crash-safe writes for sub-microsecond point-in-time (`as-of`) entity queries.

* **[Kaze-OS](https://github.com/devpryan7792/kaze-os)** — A modular Arch Linux build engine experimenting with three hyper-focused Wayland OS flavors (Hayate for gaming, Kasumi for desktop ricing, and Nagomi for daily work).

* **[hyprquickshell](https://github.com/devpryan7792/hyprquickshell)** — My active daily driver desktop environment. Arch Linux + Hyprland powered by Quickshell, Qt6/QML, and dynamic Matugen Material You theming with GPU autodetect and turnkey automation.

* **[Saknussemm](https://github.com/devpryan7792/saknussemm)** — A creative 2.5D scroll-driven subterranean exploration web engine inspired by Jules Verne.
  * Features custom volumetric lighting (god rays), normal-mapped rock strata with dynamic normal vectors, and WebGL fluid distortion shaders.

---

### 🔍 Upstream OSS Explorations

When I run into bugs or odd behavior in tools I use, I try to dig into the source and open patches upstream:

* **[hyprwm/hyprlock#1091](https://github.com/hyprwm/hyprlock/pull/1091)**: Defer auth initialization until the Wayland session lock is safely acquired.
* **[python/cpython#159081](https://github.com/python/cpython/pull/159081)**: Correct `UnicodeDecodeError` offsets in the `utf-8-sig` codec when input starts with a BOM.
* **[astral-sh/ruff#29810](https://github.com/astral-sh/ruff/pull/29810)**: Fix parser logic to avoid treating relative imports from `__future__` as future imports.
* **[janbjorge/pgqueuer#954](https://github.com/janbjorge/pgqueuer/pull/954)** *(Merged)*: Refactor driver to remove unused `tm` properties.
* **[oxpull/django-ox#149](https://github.com/oxpull/django-ox/pull/149)** *(Merged)*: Add `ox_retry` and `ox_discard` CLI commands.
* Other explorations in `hyprwm/Hyprland`, `hyprwm/hypridle`, `psycopg`, `advanced-alchemy`, and `Cap`.

---

### 💻 Tooling & Daily Environment

<p align="left">
  <img src="https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white" alt="Rust" />
  <img src="https://img.shields.io/badge/Linux_Kernel-1793d1?style=for-the-badge&logo=linux&logoColor=white" alt="Linux" />
  <img src="https://img.shields.io/badge/Wayland-00599C?style=for-the-badge&logo=wayland&logoColor=white" alt="Wayland" />
  <img src="https://img.shields.io/badge/Hyprland-00a88f?style=for-the-badge&logo=hyprland&logoColor=white" alt="Hyprland" />
  <img src="https://img.shields.io/badge/Arch_Linux-1793d1?style=for-the-badge&logo=archlinux&logoColor=white" alt="Arch Linux" />
  <img src="https://img.shields.io/badge/QEMU%2FKVM-FF6600?style=for-the-badge&logo=qemu&logoColor=white" alt="QEMU" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
</p>

---

### 📊 Activity & Telemetry

<div align="center">
  <a href="https://github.com/devpryan7792">
    <img src="https://github-readme-stats.vercel.app/api?username=devpryan7792&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0d1117&title_color=58a6ff&icon_color=79c0ff&text_color=c9d1d9" alt="GitHub Stats" width="48%" />
  </a>
  <a href="https://github.com/devpryan7792">
    <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=devpryan7792&layout=compact&theme=tokyonight&hide_border=true&bg_color=0d1117&title_color=58a6ff&text_color=c9d1d9" alt="Top Languages" width="48%" />
  </a>
</div>

<br>

<div align="center">
  <sub>Constructed with zero fluff. Always testing in QEMU.</sub>
</div>
