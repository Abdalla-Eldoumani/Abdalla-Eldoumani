<div align="center">

# Abdalla ElDoumani

**Silicon to interface. Building at every layer of the stack.**

Computer Science at the University of Calgary, B.Sc. June 2027, Dean's List

[![Portfolio](https://img.shields.io/badge/Portfolio-abdallaeldoumani.com-0A0F1C?style=for-the-badge&logo=vercel&logoColor=white)](https://abdallaeldoumani.com)
[![Resume](https://img.shields.io/badge/Resume-PDF-16181A?style=for-the-badge&logo=readdotcv&logoColor=white)](https://abdallaeldoumani.com/resume)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Abdalla%20Eldoumani-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/abdallaeldoumani/)
[![Email](https://img.shields.io/badge/Email-aamsdoumani%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:aamsdoumani@gmail.com)

</div>

I build systems software (an ARM64 operating system, a compiler, CPU and GPU math kernels) and full-stack web applications. I graduate in June 2027 and I'm open to new-grad conversations.

## Now

- **Research (PURE Award, Summer 2026):** proactive task replication for extreme edge computing, using a reputation-aware MILP model to place tasks across unreliable, user-owned devices.
- **[AArch64 Playground](https://aarch64-playground.vercel.app):** a browser-based ARMv8 emulator with a visual debugger, built for CPSC 355 students. Next.js frontend, Rust-to-WASM emulator core. I lead development.

## Selected work

Ordered by how close each project sits to the hardware.

| Layer | Project | What it is | Built with |
|---|---|---|---|
| Bare metal | [aeos](https://github.com/Abdalla-Eldoumani/aeos) | Bare-metal AArch64 OS that boots from reset to a windowed desktop: MMU, EL0 userspace via a static ELF loader, four SMP cores, an in-kernel ARP/ICMP stack, and a compositing GUI | C, ARMv8 assembly, QEMU |
| Language and VM | [qala-lang](https://github.com/Abdalla-Eldoumani/qala-lang) | Statically typed language with effect annotations and scope-bound defer: bytecode VM, ARM64 backend, published on [crates.io](https://crates.io/crates/qala-cli), with a [browser playground](https://qala-lang.vercel.app) | Rust, WASM, Next.js |
| Compute kernels | [peregrine](https://github.com/Abdalla-Eldoumani/peregrine) | Heterogeneous linear algebra for Python: AVX2 CPU kernels and an optional cuBLAS CUDA backend behind one zero-copy, NumPy-compatible API. Device-resident matmul reaches 28x NumPy; fused kernel chains reach 71x | C++, CUDA, Python |
| Network server | [rust-http-server](https://github.com/Abdalla-Eldoumani/rust-http-server) | HTTP server handling 10,000+ concurrent connections at sub-10ms latency, with JWT auth, full-text and fuzzy search, and caching that cut database load 60% | Rust, Axum, SQLite |
| Browser tools | [dossier](https://github.com/Abdalla-Eldoumani/dossier) | Privacy-first PDF toolkit: 40+ operations that run entirely on-device, shipped as a static web app and an MCP server over one shared core | TypeScript |
| Agent infrastructure | [qemu-mcp-server](https://github.com/Abdalla-Eldoumani/qemu-mcp-server) | MCP server for controlling QEMU virtual machines over QMP: lifecycle, snapshots, console I/O, memory inspection. Published on [npm](https://www.npmjs.com/package/qemu-mcp-server) | TypeScript, QEMU |

Hackathon work: [Pile](https://github.com/Abdalla-Eldoumani/Pile), an audio briefing generator that anchors every spoken line to its source paragraph (Cursor Calgary Hackathon, May 2026), and [DUST](https://github.com/Abdalla-Eldoumani/DUST), a real-time multiplayer web game (Calgary Hacks 2026).

Some repos here weren't built for a resume at all: a [tajweed trainer](https://github.com/Abdalla-Eldoumani/tajweed-trainer), a [Qur'an and sunnah browser extension](https://github.com/Abdalla-Eldoumani/islam-extension), tools for my own community.

## Where to start reading

- **Systems:** *aeos*. Start at the boot path, then the scheduler, then the compositor.
- **Languages and runtimes:** *Qala*. The bytecode VM first, then the ARM64 backend. The name is Arabic, qala, "he said": the whole idea of the language is that what you declare is what happens.
- **Performance:** *Peregrine*. The AVX2 blocking, the fused kernels, and the CPU/GPU crossover calibration. The benchmarks include the losses.
- **Web and tools:** the [playground](https://aarch64-playground.vercel.app) live, then *dossier* for how one TypeScript core ships as both a web app and an MCP server.

## Teaching

Head TA for CPSC 355 (Computer Architecture, ARMv8) at the University of Calgary in 2025-26: a class of 120+, a five-TA team, and a Gradescope autograder built on Python, Docker, and QEMU user-mode emulation so ARM64 binaries grade deterministically on x86 servers. Tutorial lead for CPSC 413 (Design and Analysis of Algorithms), where I wrote a stress-test autograder that enforces optimal asymptotic complexity.

## Stack

**Languages**

![C](https://img.shields.io/badge/C-00599C?style=flat-square&logo=c&logoColor=white)
![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![ARMv8 Assembly](https://img.shields.io/badge/ARMv8_Assembly-0091BD?style=flat-square&logo=arm&logoColor=white)

**Web**

![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)

**Systems and infrastructure**

![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![QEMU](https://img.shields.io/badge/QEMU-FF6600?style=flat-square&logo=qemu&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![CUDA](https://img.shields.io/badge/CUDA-76B900?style=flat-square&logo=nvidia&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white)

## Off hours

Football, mostly: watching it, arguing about it, and a FIFA career mode that has outlasted a few of the repos above. Beyond that, bouldering and the gym. The card at the bottom is my GitHub year, rated like a FUT player.

<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats.vercel.app/api/top-langs/?username=Abdalla-Eldoumani&layout=compact&langs_count=8&hide_border=true&theme=dark">
  <source media="(prefers-color-scheme: light), (prefers-color-scheme: no-preference)" srcset="https://github-readme-stats.vercel.app/api/top-langs/?username=Abdalla-Eldoumani&layout=compact&langs_count=8&hide_border=true">
  <img alt="Top languages" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Abdalla-Eldoumani&layout=compact&langs_count=8&hide_border=true">
</picture>

[![My GitFut card](https://gitfut.com/Abdalla-Eldoumani.png)](https://gitfut.com/Abdalla-Eldoumani?country=EG)

</div>
