# お座り

## Introduction

![osuwari](osuwari.jpg)

## Installation

Install [thefuck](https://github.com/nvbn/thefuck) using `pip`:
```bash
pip3 install thefuck
```

Place the following command in `.bash_profile`, `.bashrc`, `.zshrc` or other startup script:
```bash
function pre_osuwari () {
	printf '\033[0;32mかごめ：\033[0;31mおすわり！\033[0m\n'
}
eval $( (echo; thefuck --alias osuwari) | sed '1,/{/s/{/{ pre_osuwari;/')
```

Finish!
