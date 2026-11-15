# Mobile Application Security - Foundations and Analysis Labs

## Overview

This repository collects Android application security learning exercises, with separate directories for static and dynamic-analysis topics. The broader foundation includes Android application components, app permissions, network communication, local data protection, and secure handling of configuration values.

## Repository Structure

| Location | Description |
| --- | --- |
| `static_analysis_in_mobile_security/` | APK inspection, decompilation, application logic, and native-library review |
| `dynamic_analysis_in_mobile_security/` | Runtime-oriented challenges and documented reverse-engineering case studies |
| `0-flag.txt` through `3-flag.txt` | Root-level verification artifacts; not application source or a standalone mobile security tool |

## Foundations: Security Review of an XML Configuration

One introductory exercise presents a sample application configuration for review. The analysis topics include:

- Hardcoded API keys and encryption-related values.
- Excessive or unclear permission settings.
- Overly broad network/firewall allow rules.
- User identifiers and the handling of sensitive data.
- Validation requirements for a possible Dart XML parser: non-empty API keys, bounded timeouts, unique user IDs, and recognized firewall actions.

**Scope of evidence:** the introductory brief requests a blog post and a Dart validation program, but neither deliverable is currently committed in this repository. The items above describe the learning exercise, not a published implementation.

## Security Principles

- Minimize permissions and limit access to sensitive resources.
- Do not embed production secrets in application packages or configuration files.
- Validate configuration input and use properly scoped authorization rules.
- Protect network traffic and avoid exposing sensitive user information.
- Combine static inspection with carefully controlled runtime analysis.

## Further Reading in This Repository

The two project directories contain their own README documentation describing each exercise and the exact evidence files available. This repository documents authorized learning environments, not assessments of third-party applications.
