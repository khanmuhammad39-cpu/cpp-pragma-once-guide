# When Not to Rely Only on `#pragma once`

`#pragma once` is widely supported and very convenient, but there are cases where include guards may still be preferred.

## Prefer include guards when:

- maximum portability matters
- your team or codebase requires them
- you are teaching standard preprocessor concepts
- you want an explicit, standards-friendly mechanism

## Practical takeaway

For most modern personal and professional C++ projects, `#pragma once` is a reasonable choice.

If portability, teaching, or strict project conventions matter more, include guards are often the better option.
