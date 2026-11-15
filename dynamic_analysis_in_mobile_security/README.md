# Android Application Analysis - Runtime Concepts and Documented Case Studies

## Overview

This directory contains Android security challenges centered on application behavior, native code, cryptographic transformations, and hidden functions. The exercises introduce dynamic instrumentation concepts; the committed reports also document concrete **static reverse-engineering and Python-based reconstruction** approaches.

## Repository Files

| File | Content |
| --- | --- |
| `0-flag.txt` | Verification result for the introductory Android runtime challenge |
| `1-flag.txt`, `1-report.md` | Investigation of a JNI native method and reconstruction of its decoded output |
| `2-flag.txt`, `2-report.md` | Analysis of locally implemented XOR decryption and an intentionally inefficient Fibonacci computation |
| `3-flag.txt`, `3-report.md` | Analysis of a concealed function and its encoded byte-transformation logic |

## Case Study Highlights

### Native Library Inspection

`1-report.md` describes reviewing Java bytecode with JADX, locating a native library, inspecting exported JNI symbols, and reproducing the data transformation in Python. The report explicitly uses **offline static analysis** rather than documenting a live Frida hook.

### Local Cryptographic Logic

`2-report.md` documents an application whose encoded value is processed locally using an XOR operation with a Fibonacci-derived key. The report explains the expensive recursive calculation and demonstrates a more efficient reconstruction. It does **not** show interception of a remote server response.

### Hidden Method Investigation

`3-report.md` tracks an obfuscated function not called by the normal user interface. Decompiled code and a Python reimplementation are used to understand its decoding logic; the report does **not** record live runtime injection.

## Related Dynamic-Analysis Skills

The corresponding training material discusses Frida, Objection, ADB, native function hooks, network interception, and controlled Android emulators. These are relevant follow-up methods, **not tools claimed to have been used in the submitted reports**.

## Security Lessons

- Hiding functions or keys in a client application does not guarantee secrecy.
- Reversible local obfuscation offers limited protection against code analysis.
- Native code can still be inspected through exported symbols and disassembly.
- Technical reports should distinguish observed runtime behavior from conclusions drawn through static analysis.

Only authorized test APKs and isolated analysis environments are within this project's scope. Verification values are not reproduced in this README.
