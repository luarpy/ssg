# ssg

Custom static site generator based on the work of [romanzolotarev](https://www.romanzolotarev.com/ssg.html) and modified by [Wolfgang](https://www.youtube.com/watch?v=N_ttw2Dihn8).

## Dependencies

- lowdown or Markdown.pl
- [pup](https://github.com/EricChiang/pup)

###### Debian based

```sh
sudo apt install lowdown pup
```

## Installation

```sh
git clone https://github.com/luarpy/ssg.git
cd ssg
chmod +x ssg
```

For a fast usage place it in your PATH variable if you want to use it as a system binary:

```sh
export PATH="$PATH:$PWD"
```

or download the script directly to your personal binary directory inside your home:

```bash
curl https://raw.githubusercontent.com/luarpy/ssg/main/ssg --output "$HOME/.local/bin/ssg"; chmod +x "$HOME/.local/bin/ssg"

```



## Usage

Follow this [example](https://www.romanzolotarev.com/ssg.html#:~:text=bin/Markdown.pl%0A%24-,usage,-make%20sure%20ssg6)

```bash
ssg src/ dst/ 'Example blog' 'https://example.com'
```

If you would like to update all the articles and files in your destiny folder, you will have to remove the control file:

```bash
rm dst/.files -f; ssg src/ dst/ 'Example blog' 'https://example.com'
```

### Configuration file

It will be used if it exists under ```src/.config``` directory. Otherwise it will use the default values.
Configuration file example:

```bash
STYLESHEET="style.css"
SCRIPT="toggle.js" 
NOSCRIPT="Yes"
BUTTON_TEXT="Main page" 
DOMAIN_NAME="https://example.com" 
```



## TODO

- [ ] Remove space between tags so the file characters are less, this way I could reduce file's size 
- [ ] Generate Table of Contents for every file and append it
- [ ] Update the html header and footer with the neweer examples
