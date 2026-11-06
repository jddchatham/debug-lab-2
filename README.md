# Debug Lab 2.0

DOS reversing workbench (2026 edition). Successor to the bash
`debug-lab`. TUI (curses) + scriptable CLI. Run, capture, diff, and
disassemble DOS programs under DOSBox-X.

- `debug-lab2` — the Python workbench (this repo's main tool)
- `debug-lab`  — the original bash workbench, kept for reference

## Install

```sh
cp debug-lab2 ~/.local/bin/ && chmod +x ~/.local/bin/debug-lab2
```

Requires: Python 3, DOSBox-X with debugger at `~/.local/bin/dosbox-x`.
For `qcrack`: the `~/reverse-qcrack` pipeline and QCRACK binaries.

## Use

```
debug-lab2 tui                     interactive workbench (default)
debug-lab2 run DIR "CMDLINE"       run windowed under DOSBox-X
debug-lab2 debug DIR "CMDLINE"     run under the DOSBox-X debugger
debug-lab2 capture DIR "CMDLINE"   headless run + text-screen capture
debug-lab2 caps                    list captures
debug-lab2 diff A B                unified diff of two captures
debug-lab2 inspect FILE.EXE        MZ / DJGPP-COFF / PE header report + strings
debug-lab2 disasm FILE.COM         disassemble a .COM (org 0x100)
debug-lab2 sessions                list saved sessions
debug-lab2 qcrack                  hand off to the QCRACK case-study bench
```
