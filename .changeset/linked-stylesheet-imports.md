---
"@shadcn/lint": patch
---

Resolve a stylesheet's own `@import`s from where the file really lives. Under pnpm a package is a symlink into the store, and its dependencies are installed beside the real file, not beside the link. `no-unknown-classes` fell back to the bundled grammar for any theme that imported such a package.
