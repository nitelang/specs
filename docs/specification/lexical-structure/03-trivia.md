---
icon: lucide/hash
description: About how Nite language treats trivia in source code.
---

# Trivia
Syntax trivia represents the parts of the source code that are completely ignored by the compiler during execution but are vital for human readability.

Any kind of spaces, new lines, documentations, and comments are syntax trivia.

## Shebang
The Nite language treats *any* line that begins with `!#` as trivia till the wery line feed.