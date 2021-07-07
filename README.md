# Easy Theme
> Generate neovim theme(in lua) from yaml file.


# Installation
```bash
git clone https://github.com/Murtaza-Udaipurwala/easy-theme.nvim
cd easy-theme.nvim/
pip install -r requirements.txt
```


## Usage
- A sample template.yml is included in the repository
- The `information` and `palette` section in yml file is compylsory
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
python easy-theme.py <your_yaml_file>.yml
```
