<div align="center">

# Abdalla ElDoumani

**Silicon to interface. I like to know what the machine is doing underneath.**

Honours Computer Science at the University of Calgary, graduating June 2027, Dean's List

[![Portfolio](https://img.shields.io/badge/Portfolio-abdallaeldoumani.com-0A0F1C?style=for-the-badge&logo=vercel&logoColor=white)](https://abdallaeldoumani.com)
[![Resume](https://img.shields.io/badge/Resume-PDF-16181A?style=for-the-badge&logo=readdotcv&logoColor=white)](https://abdallaeldoumani.com/resume)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Abdalla%20Eldoumani-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/abdallaeldoumani/)
[![Email](https://img.shields.io/badge/Email-aamsdoumani%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:aamsdoumani@gmail.com)

</div>

Hi. I write systems software (kernels, emulators, a small language) and I also ship web apps, and most of what is on this page came from wanting to see what happens one layer down from wherever I was standing. I graduate in June 2027 and I am looking for a new grad software role in Canada, ideally somewhere the work touches the lower layers: developer tools, infrastructure, embedded, compilers.

## Right now

- **Head TA for CPSC 355**, the computer architecture and ARMv8 assembly course at UCalgary. Second time running it, this term for about 300 students.
- **[AArch64 Playground](https://aarch64-playground.com).** I took 355 in my second year, found it hard, and loved it. What made it hard was not the course, it was the tooling: you wrote assembly over SSH and got a segfault with no line number. So in May 2026 I spent a weekend writing an ARM64 interpreter, and three weeks later it ran real programs. It is now a browser emulator and step debugger (Rust compiled to WebAssembly, Next.js in front) that I lead with a professor and two collaborators. It is checked against the department's real servers on 50 compiled C programs, so what a student sees in the browser is what they would see on the server.
- **Honours thesis.** How well current language models write, repair, and predict ARMv8 assembly, judged by running the code instead of reading it.
- **Technical advisor for MIST** (Muslim Innovators in Science and Technology), which mostly means being the person people come to when something breaks, plus a second look at the technical side of the club's events.

Summer 2026 was two research awards: the Playground above, and a project with Prof. Sara Elsayed on where to place copies of tasks across unreliable edge devices, written as an optimization model and solved at full scale with Gurobi. We found why the published baseline dropped more tasks than it should, and the results are drafted into a paper.

## Things I have built

Ordered by how close each one sits to the hardware.

| Layer | Project | What it is | Built with |
|---|---|---|---|
| Bare metal | [aeos](https://github.com/Abdalla-Eldoumani/aeos) | An AArch64 operating system from reset to a windowed desktop: MMU, userspace via an ELF loader, four cores, an ARP and ICMP stack, a compositing GUI. Tetris ships with the kernel | C, ARMv8 assembly, QEMU |
| Language and VM | [qala-lang](https://github.com/Abdalla-Eldoumani/qala-lang) | A statically typed language where `is pure` and `is io` are promises the compiler checks. Bytecode VM, ARM64 backend, on [crates.io](https://crates.io/crates/qala-cli), with a [browser playground](https://qala-lang.vercel.app) | Rust, WASM, Next.js |
| Compute kernels | [peregrine](https://github.com/Abdalla-Eldoumani/peregrine) | Linear algebra for Python that picks the right silicon for the shape of the problem: AVX2 on the CPU, cuBLAS on the GPU, one NumPy-compatible API. Device-resident matmul reaches 28x NumPy; fused kernel chains reach 71x. The benchmarks include the cases where it loses | C++, CUDA, Python |
| Network server | [rust-http-server](https://github.com/Abdalla-Eldoumani/rust-http-server) | A REST and WebSocket server I built to learn how the real ones are put together: JWT sign-in with refresh tokens, rate limits, a job queue that retries, full text search that forgives typos. The middleware is written by hand | Rust, Axum, SQLite |
| Browser tools | [dossier](https://github.com/Abdalla-Eldoumani/dossier) | A PDF toolkit where nothing leaves your machine: 42 operations, shipped as a web app and as an MCP server from one shared core | TypeScript |
| Agent infrastructure | [qemu-mcp-server](https://github.com/Abdalla-Eldoumani/qemu-mcp-server) | Lets an AI agent drive QEMU virtual machines over QMP: boot, snapshot, console, memory. On [npm](https://www.npmjs.com/package/qemu-mcp-server) | TypeScript, QEMU |

Hackathon work: [Pile](https://github.com/Abdalla-Eldoumani/Pile), which turns your saved reading pile into an audio briefing where every spoken line points back to its source paragraph (Cursor Calgary Hackathon, May 2026), and [DUST](https://github.com/Abdalla-Eldoumani/DUST), a real time multiplayer game built in 24 hours (Calgary Hacks 2026).

Some repos here were never meant for a resume: a [tajweed trainer](https://github.com/Abdalla-Eldoumani/tajweed-trainer), a [Qur'an and sunnah browser extension](https://github.com/Abdalla-Eldoumani/islam-extension). Tools for my own community.

## If you only have ten minutes

- **Systems:** *aeos*. Start at the boot path, then the scheduler, then the compositor.
- **Languages and runtimes:** *Qala*. The bytecode VM first, then the ARM64 backend. Qala is Arabic for "he said": the idea of the language is that what you declare is what happens.
- **Performance:** *Peregrine*. The AVX2 blocking, the fused kernels, and the point where sending work to the GPU stops paying for itself.
- **Web and tools:** open the [playground](https://aarch64-playground.com) and step through a program, then look at how *dossier* ships one TypeScript core as both a web app and an MCP server.

## Teaching

I have TA'd CPSC 355 three terms running: TA in Fall 2025, Head TA in Winter 2026 for 120 students and a team of five TAs, and Head TA again now for about 300. I built the Gradescope autograders (Python, Docker, QEMU) so ARM64 programs grade the same way every time on x86 servers, and wrote the tutorials and about a hundred practice problems. In Winter 2026 I also ran the tutorials for CPSC 413 (algorithms) and wrote an autograder there that fails a solution if its asymptotic complexity is wrong, not just its output. Debugging other people's assembly every week is a big part of why everything I build tries to be legible.

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

## Off hours

Football, mostly: watching it, arguing about it, and a FIFA career mode that has outlasted a few of the repos above. Beyond that, bouldering and the gym. The card at the bottom is my GitHub year, rated like a FUT player.

<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats.vercel.app/api/top-langs/?username=Abdalla-Eldoumani&layout=compact&langs_count=8&hide_border=true&theme=dark">
  <source media="(prefers-color-scheme: light), (prefers-color-scheme: no-preference)" srcset="https://github-readme-stats.vercel.app/api/top-langs/?username=Abdalla-Eldoumani&layout=compact&langs_count=8&hide_border=true">
  <img alt="Top languages" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Abdalla-Eldoumani&layout=compact&langs_count=8&hide_border=true">
</picture>

<a href="https://gitfut.com/Abdalla-Eldoumani?country=EG"><img src="https://gitfut.com/Abdalla-Eldoumani.png" alt="My GitFut card" width="415"></a>

</div>
