<!--
Write for a reviewer who will not open the files. Short prose.
Delete any section that does not apply.
-->

## Why

<!-- One or two sentences. Name the problem, the plugin, or the language server. -->

## What changes

<!--
One picture, with a Before and an After. Draw two diagrams, Before and
After, or draw one diagram and mark the changed parts with
`classDef changed`. For a new thing, write "Before: none."

Pick the diagram with one question: does the next step depend on an input
from outside, which can come late, come wrong, or not come?
- Yes: a Mermaid state diagram (stateDiagram-v2). An outside input is a
  user action, a reply from a service or a device, a webhook, a timer, or
  a cancel. A state is a place where the thing waits, for example
  "Waiting for the server to attach" or "Waiting for the next key". An
  arrow is the event that moves it on. Draw the arrows for the bad events
  too (timeout, error, cancel, retry), because the change can go wrong
  there.
- No: a Mermaid flowchart. The procedure runs from start to end with the
  data that it has, for example how Neovim picks the server command
  (project binary first, then the global binary), or the plugin load
  order at startup. Boxes are steps, arrows mean "then", and diamonds are
  decisions on that data.
- No diagram fits (a plugin lock update, a keymap, an option value): a
  table of old and new values, a diff, or pseudocode.
Add up to three bullets for what the picture misses, including what you
left out on purpose.
-->

**Look at:** <!-- the one file or decision that needs a careful look -->

## Evidence

<!--
This repo has no CI. List the checks that you ran and their results, and
what stays unchecked. For example:
- `nvim --headless "+qa"` exits without errors.
- The changed plugin loads, for example in `:Lazy` or `:checkhealth <plugin>`.
- The changed language server attaches to a real file. Name the file and
  the server, and show `:LspInfo` output or the diagnostic that it reports.
Name the Neovim version. Say if you did not test on Linux.

A visible change (colors, layout, popups) shows before and after
screenshots, side by side. Crop to the changed area.
-->

## Merge danger

**Door:** <!-- one-way (hard to undo) or two-way (a revert and `:Lazy restore` fix it) -->
**Blast radius:** <!-- one word, e.g. none, plugin, LSP, editor -->

<!--
One or two sentences on what could break and where. The dotfiles repo links
this config to ~/.config/nvim on the Mac and on Linux hosts, so a startup
error breaks the editor on all of them. Name a dependency on a binary or
file that the dotfiles repo installs, for example ~/.config/tsrs/tsgo.
-->

## After merge

<!--
Manual steps in order. Delete if none. For example:
1. Merge the dotfiles change that this change needs, if there is one.
2. Update the nvim submodule commit in the dotfiles repo.
3. On each machine, pull and run `:Lazy restore` to match lazy-lock.json.
-->
