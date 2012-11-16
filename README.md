### F# Syntax Definitions for Sublime Text 2 ###

F# syntax definitions for [Sublime Text 2](http://www.sublimetext.com/). When installed, these provide syntax highlighting to make it easier to work with F# source code.


---
### Supports ###

- **F# source files and scripts** (`.fs`, `.fsi`, `.fsx`)
  - This file is based on [fsharp-tmbundle](https://code.google.com/p/fsharp-tmbundle/).
- **fslex** (`.fsl`) and **fsyacc** (`.fsy`)
  - These are modified versions of the ocamllex and ocamlyacc definitions which ship with Sublime Text.


---
### TODO ###

- Bugfixes
  - Some keywords and compiler directives aren't highlighted.
  - Verbatim strings are not yet supported (i.e., they're not highlighted correctly).
  - In the fslex and fsyacc definitions:
    - Some text elements are highlighted correctly (i.e., they're recognized and the correct color/style is applied), but the last character in the token isn't highlighted.
    - If the single-line comment token `//` occurs on the same line as and before the closing token of a multi-line comment `*)`, the `//` eats the rest of the line -- including the `*)`. This causes the multi-line comment not to be closed, so the rest of the file will be highlighted as if it were commented-out. For example:

      ```fsharp
      (* Some comment text, with a link below it:
         http://foobar.com/baz *)
      ```

- Future
  - Syntax highlighting for F# Interactive when used through SublimeREPL.
  - Once the bugs are fixed, I'll create a package and for this and submit it to Package Control so it can be installed from within Sublime Text.


---
### License ###

**sublime-fsharp** is released under the [Simplified BSD License](http://opensource.org/licenses/BSD-2-Clause). See the LICENSE.md file for full license text.
