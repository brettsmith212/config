# Nvim Setup

## Install [LazyVim](https://www.lazyvim.org/installation)

## Add snippet to `lua/config/keymaps.lua`
```lua
vim.keymap.set("n", "<leader>i", "<cmd> lua vim.diagnostic.open_float() <CR>")
vim.keymap.set("i", "jk", "<Esc>", { noremap = true, silent = true })
vim.keymap.set("n", "<tab>", "<cmd> bnext <CR>")
vim.keymap.set("n", "<s-tab>", "<cmd> bprevious <CR>")
```

## Add snippet to `lua/config/autocmds.lua` for auto reload w/ cli ai agents
```lua
vim.opt.autoread = true

vim.api.nvim_create_autocmd({ "FocusGained", "BufEnter", "TermClose", "WinEnter", "TabEnter" }, {
  desc = "Reload file if changed on disk when returning to Neovim or switching windows",
  command = "checktime",
})

-- Optional: notify when reload happens
vim.api.nvim_create_autocmd("FileChangedShellPost", {
  callback = function(ev)
    vim.notify(("Reloaded: %s"):format(vim.fn.fnamemodify(ev.file, ":.")), vim.log.levels.WARN)
  end,
})
```
