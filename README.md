# floating-input.nvim
Super simple Neovim floating input.

![screenshot](https://user-images.githubusercontent.com/1334962/224120029-17ad63ed-ebde-4636-aea6-deccb305ba7b.jpg)

## Why

You use Telescope or Fzf-Lua to get a nice `vim.ui.select`, and want a nice `vim.ui.input` (e.g.
handling LSP rename) too?

[Dressing](https://github.com/stevearc/dressing.nvim) works, but most of its code deals with
`vim.ui.select`, which seems slightly overkill here.

This plugin is the simplest floating window to take input.

## How

Neovim 0.9+ is required. Add `liangxianzhe/floating-input.nvim` to your plugin manager, no setup is needed.

Default is to put floating window under the cursor for LSP renaming, and at the center for other use cases. 

You can config styles, or override other window configs: 
```lua
vim.ui.input = function(opts, on_confirm)
	require("floating-input").input(opts, on_confirm, { border = 'double' })
end
```
