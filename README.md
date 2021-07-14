# EZ
> Generate neovim theme(in lua) from yaml file.


# Installation
```bash
git clone https://github.com/Murtaza-Udaipurwala/ez.nvim
cd ez.nvim/
pip install -r requirements.txt
```


# Features
- Easily generate a modularized colorscheme in lua from a yaml file
- Supports asynchronous loading
- The generated colorscheme is well written lua code providing a solid base for further extending the colorscheme
- All the highlighting can be modularized into different, more managable files


# What do I mean by async loading
- Everything you wrap around `async:` key in yaml file will be loaded asynchronously by neovim and will not block the loading of other plugins.
- In short, it will make neovim load a little bit faster.


## Usage
- A sample [template.yml](https://github.com/Murtaza-Udaipurwala/ez.nvim/blob/master/template.yml) is included in the repository
- The `information` and `palette` keys in yml file are compulsory
- The highlight group properties in yml file must be in the order "foreground_color background_color style". Any property can be skipped using '-'
- Styles:
    * i: italic
    * b: bold
    * u: underline
    * r: reverse
- Eg:
```yml
  Normal: "fg bg"
  Comment: "green - i"
```
- Everything except basic highlights and treesitter highlights can be wrapped inside `async:` key. Refer [template.yml](https://github.com/Murtaza-Udaipurwala/ez.nvim/blob/master/template.yml)
- [Example yml file](https://raw.githubusercontent.com/ChristianChiarulli/nvcode-color-schemes.vim/master/onedark.yml)
- To generate a colorscheme from the yaml file run:
```bash
python ez.py <your_yaml_file>.yml
```


# The script adds following configuration options
```lua
vim.g.transparent_background = true        -- transparent background(Default: false)
vim.g.italic_comments = true               -- italic comments(Default: true)
vim.g.italic_keywords = true               -- italic keywords(Default: true)
vim.g.italic_functions = true              -- italic functions(Default: false)
vim.g.italic_variables = true              -- italic variables(Default: false)
```


# Themes made with ez.nvim
* [darkplus](https://github.com/Murtaza-Udaipurwala/darkplus.nvim)
* [LunarVim colorschemes](https://github.com/LunarVim/Colorschemes)
