<!--
Write for a reviewer who will not open the files. Short prose.
Delete any section that does not apply.
-->

## Why

<!-- One or two sentences. Name the problem, the plugin, or the language server. -->

## What changes

<!--
One picture. Pick the smallest view that makes the point:
- A plugin lock update (lazy-lock.json): a table with the columns plugin,
  old commit, and new commit. Mark plugins that were added or removed.
- A plugin spec or option change: a diff of the spec or the options table.
- A language server change: a Mermaid flowchart of how Neovim picks the
  server command, for example project binary first, then the global binary.
- A keymap change: a table with the columns mode, keys, old action, and
  new action.
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
