# Huawei EC

**Disclaimer**: this script was written to work with model `MACH-WX9` i.e. Matebook X Pro (2018). The author is not to blame if this script(s) breaks your system.

A script that enables the use of some of Huawei PC Manager features like setting battery protection settings and fn key lock state. It works by modifying the embedded controller (EC) data.

This script requires `ioport` to be present, specifically `inb` and `outb`.

## Usage

```
$ sudo huawei_ec [get|set] [batpro|batthre|fnlk] [value]
```

* `batpro` - setting battery protection on and off
* `batthre` - setting battery threshold min and max values
* `fnlk` - setting FN key lock on and off

## References
1. [andmarios](https://aymanbagabas.com/2018/07/23/archlinux-on-matebook-x-pro.html#comment-4412527488)
2. `ec_sys` kernel module.
3. [acer_ec.pl](https://github.com/Lekensteyn/acpi-stuff/blob/master/acer_ec.pl)
4. [Using I/O ports in C programs](https://www.tldp.org/HOWTO/IO-Port-Programming-2.html)

## Credits
Thanks to [andmarios](https://disqus.com/by/andmarios/) for his debugging and finding where the battery threshold values are stored.
