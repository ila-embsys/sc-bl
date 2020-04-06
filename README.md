Syntacore RISC-V first stage bootloader
========================================

About
--------------

This package contains the Syntacore first stage bootloader (SCBL) for SCR SDK platforms.

Prerequisites
--------------

RISC-V GCC toolchain is required to compile the software.

At this fork added VS Code devcontainer with necessary toolchain in Dockerfile.

To start playing need [Visual Studio Code](https://code.visualstudio.com/)
with [Remote - Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) plugin and [Docker](https://www.docker.com/products/docker-desktop).

Build SCBL
----------

If prerequisites are done -- click "Reopen Folder in Container". After that run preconfigured build task by press Ctrl+Shift+B.

Debug SCBL
----------

To debug code [OpenOCD with Syntacore targets](https://github.com/syntacore/openocd/releases) should be started on Docker host.

```
$ openocd.exe -c gdb_port 50000 -f interface/jlink.cfg -f target/syntacore_riscv.cfg
```

Once OpenOCD started it is possible to start debugging. Use preconfigured GDB RISCV launch.
It starts connecting from docker container to host.docker.internal address and connects to OpenOCD on the host. Enjoy!