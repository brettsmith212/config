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
## Add snippet to `lua/plugins/everforest.lua` to match ghostty everforest theme
```lua
return {
  {
    "neanias/everforest-nvim",
    lazy = false,
    priority = 1000,
    config = function()
      require("everforest").setup({
        background = "hard",
        transparent_background_level = 1,
      })
      vim.cmd("colorscheme everforest")
    end,
  },
  {
    "LazyVim/LazyVim",
    opts = {
      colorscheme = "everforest",
    },
  },
}
```
## Add snippet to `lua/config/options.lua` (note the section for only remote ssh nvim)
```lua
vim.opt.relativenumber = false
---- BEGIN USE ON REMOTE SSH NVIM ----
vim.opt.clipboard = "unnamedplus"

-- OSC 52 clipboard for SSH
vim.g.clipboard = {
  name = "OSC 52",
  copy = {
    ["+"] = require("vim.ui.clipboard.osc52").copy("+"),
    ["*"] = require("vim.ui.clipboard.osc52").copy("*"),
  },
  paste = {
    ["+"] = require("vim.ui.clipboard.osc52").paste("+"),
    ["*"] = require("vim.ui.clipboard.osc52").paste("*"),
  },
---- END USE ON REMOTE SSH NVIM ----
}
```
## Add snippet to `lua/plugins/lazygit.lua`
```lua
return {
  "folke/snacks.nvim",
  keys = {
    { "<leader>gg", function() Snacks.lazygit() end, desc = "LazyGit" },
  },
}
```
## Make sure `lazyvim.json` has this extras neo-tree line to avoid double `<leader>e` file trees
```lua
{
  "extras": [
    "lazyvim.plugins.extras.editor.neo-tree"
  ],
  "install_version": 8,
  "news": {
    "NEWS.md": "11866"
  },
  "version": 8
}
```
