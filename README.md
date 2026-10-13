# FI-Mihej

**Python & C/C++ Team Lead**  
Building high-performance OSS systems  
Async • multiprocessing • shared memory • LLM infrastructure  

---

## Focus

- High-performance Python systems (beyond typical GIL-bound design)
- Inter-process communication (IPC) with minimal overhead
- Shared memory architectures
- Async runtimes and event loop engineering
- Systems-level optimization (C/C++ / Cython / low-level integrations)

---

## Open Source Contributions

Contributor to:
- Since Jan 2023: [NiceGUI](https://github.com/zauberzeug/nicegui) ![GitHub Repo stars](https://img.shields.io/github/stars/zauberzeug/nicegui): I found a key issue in client-server event synchronization for interactive UI components (such as text editors). I identified the root cause, fixed it, and improved the overall mechanism of client-server event synchronization.
- Since Sep 2021: [Kivy](https://github.com/kivy/kivy) ![GitHub Repo stars](https://img.shields.io/github/stars/kivy/kivy): [Authored a fix](https://github.com/kivy/kivy/pull/7619) for an important Windows issue in [Kivy's](https://github.com/kivy/kivy) core (included via an [upstream PR](https://github.com/kivy/kivy/pull/7637)).
- Since Jun 2024: [Billion Row Challenge (Python)](https://github.com/ifnesi/1brc) ![GitHub Repo stars](https://img.shields.io/github/stars/ifnesi/1brc) - Python section of [The One Billion Row Challenge](https://github.com/gunnarmorling/1brc) ![GitHub Repo stars](https://img.shields.io/github/stars/gunnarmorling/1brc): I improved the performance of the pure Python implementations (for both CPython and PyPy) by an additional 10–20% (depending on the exact CPython and PyPy version).
- Since Jul 2026: [awesome-mcp-servers](https://github.com/punkpeye/awesome-mcp-servers) ![GitHub Repo stars](https://img.shields.io/github/stars/punkpeye/awesome-mcp-servers): my [Text File Read And Refactor MCP](https://github.com/FI-Mihej/text_file_read_and_refactor_mcp) and [CodebaseAgent-MCP](https://github.com/FI-Mihej/codebase-agent-mcp) have successfully passed automated analysis and manual review, qualifying them for inclusion in the list. I'm happy to be among the ![Contributors](https://img.shields.io/github/contributors-anon/punkpeye/awesome-mcp-servers) top developers of open-source MCP servers and MCP clients on GitHub.

---

## Key Projects

### [InterProcessPyObjects](https://github.com/FI-Mihej/InterProcessPyObjects) ![GitHub Repo stars](https://img.shields.io/github/stars/FI-Mihej/InterProcessPyObjects) (Part of the [Cengal](https://github.com/FI-Mihej/Cengal); Development started in Sep 2023; First released as a standalone project in May 2024)

High-performance IPC via shared memory.

- Zero/low serialization overhead approach
- Seamless sharing and mutation of Python objects across processes
- Supports:
  - NumPy arrays
  - Torch tensors
  - custom classes (including dataclasses)
  - objects with methods
  - asyncio integration

**Core idea:**  
Move away from serialization-heavy IPC → toward shared-memory object models with controlled mutation.

**Implementation stack:**  
Python + [Cengal](https://github.com/FI-Mihej/Cengal) (Python, Cython, C)

---

### [Cengal](https://github.com/FI-Mihej/Cengal) ![GitHub Repo stars](https://img.shields.io/github/stars/FI-Mihej/Cengal) (Development started in 2012; First released in Sep 2016)

Multi-domain high-performance Python toolkit.

Includes:
- Runtime bytecode manipulation
- True shared memory primitives
- Async integrations:
  - LMDB
  - Tkinter
  - wxPython
  - PySide / PyQt
- Custom async loop with near preemptive multitasking (single thread)
- Advanced introspection & text parsing tools

**Implementation stack:**  
Python + Cython + C/C++ + Nim + Go

---

### [Bensbach](https://github.com/FI-Mihej/Bensbach) ![GitHub Repo stars](https://img.shields.io/github/stars/FI-Mihej/Bensbach) (Development started in Nov 2015; First released in Sep 2016)

Unreal Engine 3 (UE3) compiler and decompiler for game modding.

Decompiles bytecode to, and compiles from, a simple to use Lisp-like custom language.

Used to implement the [XCOM: EW mod: "Realistic Damage Model" at Nexus Mods](https://www.nexusmods.com/xcom/mods/663); [XCOM: EW mod: "Realistic Damage Model" at Github](https://github.com/FI-Mihej/Realistic-Damage-Model-mod-for-Long-War)

**Implementation stack:**  
Python + [Cengal](https://github.com/FI-Mihej/Cengal)

---

## MCP servers

### [CodebaseAgent-MCP](https://github.com/FI-Mihej/codebase-agent-mcp) (Development started in Jun 2026; First released in Jul 2026)

[![Listed in Awesome MCP Servers](https://img.shields.io/badge/Awesome%20MCP%20Servers-listed-2ea44f)](https://github.com/punkpeye/awesome-mcp-servers) [![CodebaseAgent-MCP MCP server – quality and maintenance score on Glama](https://glama.ai/mcp/servers/FI-Mihej/codebase-agent-mcp/badges/score.svg)](https://glama.ai/mcp/servers/FI-Mihej/codebase-agent-mcp)

A sub-harness (both an MCP server and an MCP client). Delegates documentation and source code analysis, as well as interactions with related context-providing MCP servers, to a local or inexpensive OpenAI-compatible LLM. Drastically reduces token usage and context size for coding agents on the top-tier LLM.

**Core idea:**  
Let a cheap/local LLM explore docs/code. Let a top-tier LLM write code.

**Implementation stack:**  
Python + [Cengal](https://github.com/FI-Mihej/Cengal) + [Text File Read And Refactor MCP](https://github.com/FI-Mihej/text_file_read_and_refactor_mcp)

---

### [Text File Read And Refactor MCP](https://github.com/FI-Mihej/text_file_read_and_refactor_mcp) (Development started in Jun 2026; First released in Jul 2026)

[![Listed in Awesome MCP Servers](https://img.shields.io/badge/Awesome%20MCP%20Servers-listed-2ea44f)](https://github.com/punkpeye/awesome-mcp-servers) [![text_file_read_and_refactor_mcp MCP server](https://glama.ai/mcp/servers/FI-Mihej/text_file_read_and_refactor_mcp/badges/score.svg)](https://glama.ai/mcp/servers/FI-Mihej/text_file_read_and_refactor_mcp)

Token-efficient Python stdio MCP server exposing safe text-file search, reading, and refactoring tools. Tools automatically resolve the file BOM and codepage; edit tools save files with their original encoding and BOM.

**Core idea:**  
Exports a simplified version of the `cengal.text_processing.*` modules from the [Cengal](https://github.com/FI-Mihej/Cengal) library.

**Implementation stack:**  
Python + [Cengal](https://github.com/FI-Mihej/Cengal)

---

## Engineering Direction

- Reducing Python overhead via architecture, not micro-optimizations
- Treating IPC as a first-class performance domain
- Bridging high-level ergonomics with low-level control
- Designing systems that scale beyond "standard async patterns"

---

## Tech Stack

**Languages:**  
Python, C/C++, Nim  

**Domains:**  
- Async systems
- IPC / shared memory
- Systems programming
- Performance engineering

---

## Contact / Work

- Open for high-impact system-level work
- Focus: performance-critical backends, infra, unconventional architectures
