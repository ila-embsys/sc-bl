FROM archlinux

RUN pacman -Syy \
    && pacman -S --noconfirm \
    riscv64-elf-gcc \
    riscv64-elf-gdb \
    riscv64-elf-newlib \
    make \
    libelf \
    util-linux
