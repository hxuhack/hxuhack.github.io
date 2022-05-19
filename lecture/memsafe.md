|[<b>Home</b>](https://hxuhack.github.io/) | [<b>Publications</b>](publication/list) | [<b>Artisan-Lab</b>](lab/page) | [<b>Beauty-Fudan</b>](../photo/page) | [<b>Misc</b>](misc/list) |

### Lecture Notes

#### Part1: Foundations of Memory Safety 
- Week1: [Course Introduction](memsafe/L0-course_intro.pdf)
- Week1: [Buffer Overflow](memsafe/L1-buffer_overflow.pdf)
- Week2: [Memory Allocation](memsafe/L2-mem_allocation.pdf)
- Week3: [Heap Attack and Protection](memsafe/L3-heap_attack.pdf)
- Week4: [Memory Exhaustion and Exception Handling](memsafe/L4-memory_exhaustion.pdf)
- Week5: [Concurrent Memory Access](memsafe/L5-concurrent_access.pdf)

#### Part2: Rust Programming Language
- Week6: [Rust Ownership-based Memory Management](memsafe/L6-Rust_OBRM.pdf)
- Week7: [Rust Type System](memsafe/L7-Rust_Type_System.pdf)
- Week8: [Rust Concurrency](memsafe/L8-Rust_Concurrency.pdf)
- Week9: [Rust Functional Programming](memsafe/L9-Rust_Functional_Programming.pdf)
- Week10: [Rust Compiler Design](memsafe/L10-Rust_Compiler.pdf)
- Week11: [Rust Compiler Techniques (by Guest Speaker)](memsafe/L11-compiler_tech.pdf)

#### Part3: Advanced Topic for Memory Safety
Due to Covid-19, we have to rearrange the course materials.

- Week12: [Dynamic Analysis of Rust Programs](memsafe/L12-Dynamic_Analysis.pdf)
- Week13: [Static Analysis of Rust Programs](memsafe/L13-Static_Analysis.pdf)
- Week14: Presentation (by Students)

### Reading List

**Empirical**
- Qin, Boqin, Yilun Chen, Zeming Yu, Linhai Song, and Yiying Zhang. "[Understanding memory and thread safety practices and issues in real-world Rust programs](https://dl.acm.org/doi/pdf/10.1145/3385412.3386036)." In Proceedings of the 41st ACM SIGPLAN Conference on Programming Language Design and Implementation, pp. 763-779. 2020.
- Evans, Ana Nora, Bradford Campbell, and Mary Lou Soffa. "[Is Rust used safely by software developers?](https://ieeexplore.ieee.org/abstract/document/9283950)." In 2020 IEEE/ACM 42nd International Conference on Software Engineering (ICSE), pp. 246-257. IEEE, 2020.
- Popescu, Natalie, Ziyang Xu, DAVID I. AUGUST, and AMIT LEVY. "[Safer at any speed: automatic context-aware safety enhancement for Rust](http://www.amitlevy.com/papers/nader-oopsla21.pdf)." Proceedings of the ACM on Programming Languages 5, no. OOPSLA (2021): 103.
- VanHattum, Alexa, Daniel Schwartz-Narbonne, Nathan Chong, and Adrian Sampson. "[Verifying Dynamic Trait Objects in Rust](https://www.cs.cornell.edu/~avh/dyn-trait-icse-seip-2022-preprint.pdf)." ICSE-SEIP, 2022.

**Static Analysis**
- Yechan Bae, Youngsuk Kim, Ammar Askar, Jungwon Lim, and Taesoo Kim. "[Rudra: Finding Memory Safety Bugs in Rust at the Ecosystem Scale](https://dl.acm.org/doi/pdf/10.1145/3477132.3483570)." In Proceedings of the ACM SIGOPS 28th Symposium on Operating Systems Principles, pp. 84-99. 2021.
- Zhuohua Li, Jincheng Wang, Mingshen Sun, and John CS Lui. "[MirChecker: Detecting Bugs in Rust Programs via Static Analysis](https://dl.acm.org/doi/pdf/10.1145/3460120.3484541)." In Proceedings of the 2021 ACM SIGSAC Conference on Computer and Communications Security, pp. 2183-2196. 2021.
- 

**Formal Method**
- Ralf Jung, Jacques-Henri Jourdan, Robbert Krebbers, and Derek Dreyer. "[RustBelt: Securing the foundations of the Rust programming language](https://dl.acm.org/doi/pdf/10.1145/3158154)." Proceedings of the ACM on Programming Languages 2, no. POPL (2017): 1-34.
- Dang, Hoang-Hai, Jacques-Henri Jourdan, Jan-Oliver Kaiser, and Derek Dreyer. "[RustBelt meets relaxed memory](https://dl.acm.org/doi/pdf/10.1145/3371102)." Proceedings of the ACM on Programming Languages 4, no. POPL (2019): 1-29.
- Jung, Ralf, Hoang-Hai Dang, Jeehoon Kang, and Derek Dreyer. "[Stacked borrows: an aliasing model for Rust](https://dl.acm.org/doi/pdf/10.1145/3371109)." Proceedings of the ACM on Programming Languages 4, no. POPL (2019): 1-32.
- Matsushita, Yusuke, Takeshi Tsukada, and Naoki Kobayashi. "[RustHorn: CHC-Based Verification for Rust Programs](https://library.oapen.org/bitstream/handle/20.500.12657/37721/2020_Book_ProgrammingLanguagesAndSystems.pdf?sequence=1#page=498)." In ESOP, pp. 484-514. 2020.

**Isolation**
- Rivera, Elijah, Samuel Mergendahl, Howard Shrobe, Hamed Okhravi, and Nathan Burow. "[Keeping Safe Rust Safe with Galeed](https://dl.acm.org/doi/fullHtml/10.1145/3485832.3485903)." In Annual Computer Security Applications Conference, pp. 824-836. 2021.
- Peiming Liu, Gang Zhao, and Jeff Huang. "[Securing unsafe rust programs with XRust](https://dl.acm.org/doi/pdf/10.1145/3377811.3380325)." In Proceedings of the ACM/IEEE 42nd International Conference on Software Engineering, pp. 234-245. 2020.
- Benjamin Lamowski, Carsten Weinhold, Adam Lackorzynski, and Hermann Härtig. "[Sandcrust: Automatic sandboxing of unsafe components in rust](https://dl.acm.org/doi/pdf/10.1145/3144555.3144562)." In Proceedings of the 9th Workshop on Programming Languages and Operating Systems, pp. 51-57. 2017.

**Other Language**
- Emre, Mehmet, Ryan Schroeder, Kyle Dewey, and Ben Hardekopf. "[Translating C to safer Rust](https://dl.acm.org/doi/pdf/10.1145/3485498)." Proceedings of the ACM on Programming Languages 5, no. OOPSLA (2021): 1-29.
- Sammler, Michael, Rodolphe Lepigre, Robbert Krebbers, Kayvan Memarian, Derek Dreyer, and Deepak Garg. "[RefinedC: automating the foundational verification of C code with refined ownership types](https://dl.acm.org/doi/pdf/10.1145/3453483.3454036)." In Proceedings of the 42nd ACM SIGPLAN International Conference on Programming Language Design and Implementation, pp. 158-174. 2021.


