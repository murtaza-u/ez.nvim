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
- The generated colorscheme is well written lua code providing a solid base for further extending the colorscheme
- All the highlighting can be modularized into different, more managable files


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
