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
- Since Jun 2024: [Billion Row Challenge (Python)](https://github.com/ifnesi/1brc) - Python section of [The One Billion Row Challenge](https://github.com/gunnarmorling/1brc) ![GitHub Repo stars](https://img.shields.io/github/stars/gunnarmorling/1brc): I improved the performance of the pure Python implementations (for both CPython and PyPy) by an additional 10–20%.

---

## Key Projects

### [InterProcessPyObjects](https://github.com/FI-Mihej/InterProcessPyObjects) (Part of the [Cengal](https://github.com/FI-Mihej/Cengal); first released as a standalone project in May 2024)

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

---

### [Cengal](https://github.com/FI-Mihej/Cengal) (First released in Sep 2016)

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

## MCP servers

### [CodebaseAgent-MCP](https://github.com/FI-Mihej/codebase-agent-mcp) (First released in Jul 2026)

A sub-harness (both an MCP server and an MCP client). Delegates documentation and source code analysis, as well as interactions with related context-providing MCP servers, to a local or inexpensive OpenAI-compatible LLM. Drastically reduces token usage and context size for coding agents on the top-tier LLM.

**Core idea:**  
Let a cheap/local LLM explore docs/code. Let a top-tier LLM write code.

---

### [Text File Read And Refactor MCP](https://github.com/FI-Mihej/text_file_read_and_refactor_mcp) (First released in May 2026)

Token-efficient Python stdio MCP server exposing safe text-file search, reading, and refactoring tools. Tools automatically resolve the file BOM and codepage; edit tools save files with their original encoding and BOM.

Exports a simplified version of the `cengal.text_processing.*` modules from the [Cengal](https://github.com/FI-Mihej/Cengal) library.

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
