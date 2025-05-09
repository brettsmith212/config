# Nvim Setup

## Install [LazyVim](https://www.lazyvim.org/installation)

## Add snippet to `lua/config/keymaps.lua`
```
vim.keymap.set("n", "<leader>i", "<cmd> lua vim.diagnostic.open_float() <CR>")
vim.keymap.set("i", "jk", "<Esc>", { noremap = true, silent = true })
vim.keymap.set("n", "<tab>", "<cmd> bnext <CR>")
vim.keymap.set("n", "<s-tab>", "<cmd> bprevious <CR>")
vim.keymap.set("n", "<leader>x", "<cmd> bd <CR>")
```
