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
- [NiceGUI](https://github.com/zauberzeug/nicegui)
- [Billion Row Challenge (Python)](https://github.com/ifnesi/1brc)

[Authored a fix](https://github.com/kivy/kivy/pull/7619) for an important Windows issue in [Kivy's](https://github.com/kivy/kivy) core (included via an [upstream PR](https://github.com/kivy/kivy/pull/7637)).

---

## Key Projects

### [InterProcessPyObjects](https://github.com/FI-Mihej/InterProcessPyObjects)

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

### [Cengal](https://github.com/FI-Mihej/Cengal)

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
Python + Cython + C/C++ + Nim + Go (where performance matters)

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
