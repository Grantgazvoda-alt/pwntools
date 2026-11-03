# pwntools — Forked for Grant's Toolkit

**Original:** pwntools (Gallopsled) — https://github.com/Gallopsled/pwntools
**Forked:** 2026-11-03
**Language:** Python
**Stars (upstream):** ~8,000

## What it is

The CTF framework and exploit development library. Tubes for process/network I/O, ELF parsing, ROP gadget finding, shellcode assembly, and crypto utilities.

## Why it's here

Exploit development backbone for binary challenges and when PHP sandbox escapes require shellcode or ROP. The `pwn` module is the standard for CTF solve scripts.

## Quick start

```python
from pwn import *

context.binary = elf = ELF("/path/to/binary")
p = process(elf.path)
p.sendline(b"A" * 72 + p64(elf.symbols["win"]))
p.interactive()
```

## Related forks

- RsaCtfTool — crypto-specific CTF attacks
- php2shell PoC — PHP memory-safety research
- hexstrike-ai — agent orchestration over pwntools and friends

## Scope note

CTF labs, authorized engagements, and defensive research only.
