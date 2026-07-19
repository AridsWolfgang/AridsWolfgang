```c
char *whoami = "aridswolfgangx";

struct {
    char *role;
    char *stack[6];
    char *domains[4];
} profile = {
    .role    = "systems software engineer",
    .stack   = {"c", "c++", "x86 assembly", "javascript/typescript", "python", "bash"},
    .domains = {"kernel", "fuzzing", "reverse engineering", "binary analysis"},
};
```

---

```nasm
; projects

crucible:   db "c, nasm, win32 — bare-metal hybrid fuzzing", 0
tcpeek:     db "c, networking, tui — multi-threaded port scanner", 0
dns_info:   db "python, dns, ci/cd — resolution toolkit", 0
forge:      db "c, sockets, workshop — systems workshop", 0
```

**crucible** — `c` `nasm` `win32`
bare-metal hybrid fuzzing framework. coverage instrumentation,
mutation engine, debug api harness, crash triage.

```
$ ./crucible --target parser --seed test.bin
⮡ crash #12 (eip=0x41414141)
```

[source](https://github.com/AridsWolfgang/Crucible)

**tcpeek** — `c` `networking` `tui`
multi-threaded port scanner. 300 concurrent workers, non-blocking
connect+select, cross-platform, service fingerprinting.

```
$ tcpeek scan.me 1-1000 -t 200
⮡ open: 22 (ssh) 80 (http) 443 (https)
```

[source](https://github.com/AridsWolfgang/TCPeek)

**dns_information** — `python` `dns` `ci/cd`
dns resolution toolkit. 16 record types, dnssec, doh, bulk concurrent
resolution, global propagation checks.

```
$ dns lookup example.com --type mx --json
⮡ 5 records · 0.34s
```

[source](https://github.com/AridsWolfgang/DNS_Information)

**forge** — `c` `sockets` `workshop`
progressive systems workshop. echo server, mini shell, cli todo with
binary persistence, port scanner with raw headers.

```
$ ./portscan 10.0.0.0/24 1-1024
⮡ 42 hosts up · 156 ports open
```

[source](https://github.com/AridsWolfgang/Forge)

---

```c
typedef struct {
    bool operating_systems;
    bool fuzzing;
    bool reverse_engineering;
    bool offensive_security;
    bool formal_methods;  // TODO
} interests;
```

```
$ cat ~/reading.md
the art of unix programming — eric s. raymond
```

```nasm
; contact

email:     db "aridswolfgangx@proton.me", 0
github:    db "github.com/AridsWolfgang", 0
x:         db "x.com/AridsWolfgangX", 0
linkedin:  db "linkedin.com/in/0xaridswolfgangx", 0
medium:    db "medium.com/@aridswolfgang", 0
web:       db "aridswolfgangx.vercel.app", 0
```

---

```nasm
; first, solve the problem. then, write the code.
```
