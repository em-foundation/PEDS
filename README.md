# PEDS

**PEDS** is a repository of platform and platform-element declarations used by EM Foundation benchmark and measurement repositories.

A declaration is an ordinary Markdown document with a stable URL. Other repositories may reference that URL to identify a complete platform or one of the declarations from which it is composed.

## Repository Structure

```text
PEDS/
    elements/
    platforms/
```

- `elements/` contains reusable declarations for hardware, boards, software, power sources, and other platform-related entities.
- `platforms/` contains complete platform declarations intended to be referenced by benchmark capture folders.

The internal organization of `elements/` is intentionally minimal and may evolve as real declarations are added.

## Platform References

A benchmark capture identifies its platform through a `.platform` file containing one declaration URL:

```text
https://github.com/em-foundation/PEDS/blob/main/platforms/nrf54l15-zephyr.md
```

The URL is the platform identity. The declaration at that location may be refined over time, but its essential meaning should remain stable.

Platform declarations may also reference declarations outside this repository.

## Declaration Composition

Declarations may include one or more `Based on` links:

```md
# Nordic nRF54L15 DK · Zephyr

- Based on [Nordic nRF54L15 DK](...)
- Based on [Zephyr](...)

- CPU clock: 128 MHz
- LF clock source: LFXO
- DC-DC converter: enabled
```

Composition is defined by links in the Markdown documents, not by the folder hierarchy.

Recommended conventions:

- list `Based on` links first
- list local facts, additions, and exceptions next
- list external documentation links last
- use **Exception**, **Addition**, and **Note** labels when they improve clarity

## Stability

PEDS is intended to provide stable declaration URLs, not immutable documents.

Git history preserves changes over time. If stronger versioning is needed later, declarations may be referenced through tags, releases, or commit-specific URLs.

## Status

This repository is being populated incrementally. Its structure and declaration conventions will evolve from actual platform use rather than from a pre-defined taxonomy.
