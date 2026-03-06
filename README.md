# PGM Operating System

Un semplice sistema operativo Unix-like per x86-64.

## Prerequisiti

```bash
# Ubuntu/Debian
sudo apt install build-essential grub-pc-bin xorriso qemu-system-x86 gcc-multilib

# Fedora
sudo dnf install gcc grub2-tools xorriso qemu-system-x86 glibc-devel.i686
```

## Compilazione

```bash
make all       # Compila il kernel e crea l'ISO
make qemu      # Esegui su QEMU
make clean     # Ripulisci
```

## Struttura del progetto

```  
pgm/  
├── kernel/  
│   ├── boot.s              # Bootloader Multiboot  
│   ├── main.c              # Kernel main  
│   ├── vga.c               # Driver VGA  
│   ├── include/vga.h       # Header VGA  
│   ├── linker.ld           # Linker script  
│   └── Makefile  
├── iso/                    # ISO directory  
├── Makefile                # Build principale  
└── README.md  
```

## TODO
- [ ] Memory management (paging, virtual memory)
- [ ] Interrupt handling
- [ ] Process/Task management
- [ ] File system
- [ ] Shell
- [ ] User programs

## Licenza MIT