# おすわり

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
eval $( (echo; thefuck --alias osuwari) | sed '1,/{/s/{/{ pre_osuwari; /' )
```

Finish! (You need to start a new shell session)

## Example

```
bash-4.4$ puthon
bash: puthon: command not found
bash-4.4$ osuwari
かごめ：おすわり！
python [enter/↑/↓/ctrl+c]
Python 2.7.15rc1 (default, Nov 12 2018, 14:31:15) 
[GCC 7.3.0] on linux2
Type "help", "copyright", "credits" or "license" for more information.
>>> 
```