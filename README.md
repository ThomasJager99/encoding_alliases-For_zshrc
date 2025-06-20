# ZSH Encoding Aliases

This is a tiny helper tool for encoding conversion inside your ZSH 
terminal. And after using a comand you receave 2 files - 1 original,
2nd encoded in UTF-8/Windows-1251This is a tiny helper tool for encoding conversion inside your ZSH terminal.  
After running a command, you get two files: the original and a new one encoded in UTF-8 or Windows-1251.

It contains two simple shell functions:

- `win2utf` — converts a file from Windows-1251 to UTF-8
- `utf2win` — converts a file from UTF-8 to Windows-1251


##Mount 

1. Open nano ~/.zshrc
2. Copy/paste this at the end of your zshrc:
# === Encoding Aliases ===
win2utf() {
    iconv -f WINDOWS-1251 -t UTF-8 "$1" > "$1".utf8.txt
}

utf2win() {
    iconv -f UTF-8 -t WINDOWS-1251 "$1" > "$1".win1251.txt
}


3.Exit zshrc with Ctrl + X and save result Y. 
4. Run source ~/.zshrc to reload shell confog and now you can use it. 



## Usage

Just run:

```bash
win2utf your_file.txt
