# The Core of How Computers Actually Work 

## Number Systems – Binary, Decimal,and Hex. 

### Binary – The Machine Language

Binary is how computers talk. Just `1`s and `0`s.
Why? Because under the hood, it’s all just **voltage**.

* High voltage? That’s a `1`.
* Low voltage? That’s a `0`.

This is *literally* how CPUs work. Billions of microscopic transistors flipping on and off.

### Decimal – The Human Language

What we use daily: `0–9`.
Easy for humans, **useless for machines** (unless it’s converted).

### Hexadecimal – The Shortcut Language

Why do we even need hex? Because binary is long and ugly.

* `11110000` in binary → `F0` in hex.
  It’s just a **cleaner way to read binary**, especially in memory dumps or file headers.

> You’ll see hex everywhere in cyber — in malware analysis, memory forensics, file carving. Learn it now.

---

## Bits, Bytes, and Storage – What Does “Size” Actually Mean?

You hear things like “this file is 1MB” or “my SSD is 512GB” — but what does that even mean?

Here’s the breakdown:

| Name   | Value       |
| ------ | ----------- |
| 1 bit  | Just 0 or 1 |
| 1 byte | 8 bits      |
| 1 KB   | 1024 bytes  |
| 1 MB   | 1024 KB     |
| 1 GB   | 1024 MB     |

### ASCII – Turning Characters into Binary

Every letter, symbol, and number you type is stored as a number.

* Example: `'A'` = `65` in decimal = `01000001` in binary.

Why care? Because when you’re doing memory forensics or analyzing traffic, you’ll literally *see* raw binary or hex. It’s not gibberish — it’s **characters, data, and code**.

---

## Transistors, Logic Gates, and How the CPU "Thinks"

Let’s get deeper.

### Transistors – The Real MVP

They’re like switches — ON (1) or OFF (0).
Modern CPUs have **billions** of them flipping per second.

### Logic Gates – Turning Bits into Logic

These are built using transistors. Think of them as **tiny decision - makers**.

| Gate Type | What It Does                 |
| --------- | ---------------------------- |
| AND       | 1 only if both inputs are 1  |
| OR        | 1 if any input is 1          |
| NOT       | Flips the bit (1 → 0, 0 → 1) |
| XOR       | 1 if inputs are *different*  |

> CPUs literally use these gates to calculate, compare, and make decisions.

### Voltage – The Physical Bit

Back in the day, high voltage was 5V = `1`, 0V = `0`.
Now it's way lower due to efficiency and hardware evolution.
Still, **a 1 is just a voltage, and that’s what flips a transistor**.

---

## ISA – The CPU’s Rulebook

### What’s an ISA?

ISA = **Instruction Set Architecture**.
It’s the list of instructions your CPU understands. Think:

* `MOV`, `ADD`, `JMP`, `PUSH`, etc.

Different CPUs speak different instruction sets:

* Intel = x86 / x64
* Mobile = ARM
* Hackers love MIPS, RISC-V, etc.

### Registers – Tiny Storage Inside the CPU

Every CPU has these tiny boxes where it temporarily stores data while it’s working. They’re fast. They matter. You’ll see them all the time in reverse engineering or exploit development.

> Wanna break something at the assembly level? Better understand what instructions and registers do first.

---

## Programming Languages, Compilers, and Interpreters

### Programming Languages

You write code in C, Python, or Java. But CPUs don’t understand that.
They need **binary**.

So we use:

### Compiler – "Translate it all at once"

* Turns your code into machine code in one go.
* Fast to run, but if there’s an error? You fix it after it compiles.
* Example: C, C++

### Interpreter – "Translate line by line"

* Runs your code as it reads it.
* Slower, but better for testing/fixing stuff.
* Example: Python, JavaScript

> You’ll need both. Hackers love Python scripts and C payloads. Learn both styles of execution.

---

## Magic Bytes and File Headers – The Real Identity of Files

### File Headers

The **first few bytes** of a file tell the system what it actually is.
You can rename `malware.exe` to `document.pdf` — but the header won't lie.

| File Type | Magic Bytes (Hex) |
| --------- | ----------------- |
| .exe      | `4D 5A` (`MZ`)    |
| .jpg      | `FF D8 FF`        |
| .pdf      | `25 50 44 46`     |

These are called:

### Magic Numbers (aka Magic Bytes)

* Unique hex values at the start of a file.
* Let forensic tools figure out file types, even if extensions are faked.

> You’ll use this for **malware analysis**, **digital forensics**, and **file carving**.

---

## Abstraction – Hiding All the Chaos

Imagine having to manually flip every bit when saving a file or typing a command. You’d lose your mind. That’s why abstraction exists.

### Examples:

* You don’t need to know binary to type a Google search.
* You don’t need to write machine code to build an app.
* You don’t need to manage RAM directly to play a YouTube video.

That’s **abstraction** — it hides the low level stuff, so you can just... use the thing.

> But cybersecurity people? We *look underneath* the abstraction. That’s where the vulnerabilities live.

---

## Final Notes

If you made it this far — thanks for reading.
 
This writeup is something I created to really understand how computers work at the lowest level before jumping into cybersecurity head first. I’m not an expert yet, so if you spot any mistakes, outdated info, or just wanna talk tech — feel free to reach out.

Connect with me on LinkedIn:[Check out my profile](https://www.linkedin.com/in/mihindi-gunawardana-110866370/)

Also, massive shoutout to TCM Security for their Practical Help Desk course.
That course helped me finally get it — not just memorize it.

[Check out the course here](https://academy.tcm-sec.com/p/practical-help-desk)


