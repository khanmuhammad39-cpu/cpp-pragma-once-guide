# C++ Guide: When to Use `#pragma once` and When Not To

This repository explains:

- what `#pragma once` does
- why multiple header inclusion causes problems
- how `#pragma once` compares with include guards
- when `#pragma once` is a good choice
- when include guards may be the better choice

## Why this matters

In C++, header files are often included indirectly through other headers.  
Without protection, the same declarations may be included more than once in the same translation unit, causing redefinition errors.

## What this repo contains

- `examples/01_no_protection/`  
  A broken example with no protection against multiple inclusion

- `examples/02_with_pragma_once/`  
  The same example fixed using `#pragma once`

- `examples/03_with_include_guards/`  
  The same example fixed using include guards

- `examples/04_when_not_to_rely_on_pragma_once/`  
  Notes on when include guards may be safer or preferred

## Rule of thumb

Use `#pragma once` in most modern C++ projects for simplicity.

Prefer include guards when:
- portability is critical
- a project or team requires them
- you want to explicitly teach how the preprocessor works

## Quick comparison

| Approach | Pros | Cons |
|---|---|---|
| `#pragma once` | Short, clean, easy to read | Not part of the formal standard |
| Include guards | Standard, portable, explicit | More verbose |

## Goal

This repo is meant to be beginner-friendly and practical, with small examples that make the difference easy to see.
