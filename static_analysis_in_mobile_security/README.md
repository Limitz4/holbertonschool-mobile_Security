# Android Static Analysis - APK and Native Code Exercises

## Overview

This project explores Android APK structure and application behavior through non-executing inspection. The exercises introduce decompilation, manifest and resource review, application/backend communication concepts, and the boundary between Java/Kotlin code and native libraries.

## Guided Challenges

| Artifact | Analysis subject |
| --- | --- |
| `0-flag.txt` | Recovering input-validation logic and hidden data from a decompiled APK |
| `1-flag.txt` | Understanding how an Android client prepares JSON data and communicates with a backend over HTTP |
| `2-flag.txt` | Interpreting compiled logic and considering mathematical or algorithmic optimizations |
| `3-flag.txt` | Investigating a native `.so` library and its interaction with Android code through JNI |

## Main Techniques

- Examining `AndroidManifest.xml`, DEX bytecode, resources, and embedded strings.
- Using tools such as JADX and apktool to obtain readable application representations.
- Following conditional checks, encoded values, and code paths related to user input.
- Understanding Java Native Interface calls and native shared-library exports.
- Recognizing the security implications of unnecessary permissions or unprotected communications.

## Repository Evidence

The four `*-flag.txt` files record verification results. The target APKs, extracted source trees, complete investigation reports, and runnable analysis tools are not included in this directory. The HTTP, optimization, and JNI topics are therefore described as exercises, **not** as code implementations stored in this repository.

## Defensive Takeaways

Static APK analysis can identify risky permissions, embedded data, and logic that deserves closer review. It provides a foundation for secure Android development and for deciding what should be tested dynamically in a controlled environment.
