**pyloc** (Python Lines of Code) is a CLI app written in Python to print the true number of lines of Python code in a project directory or file.
Excludes # comments, docstring lines and pure whitespace lines.

![pandas](https://github.com/user-attachments/assets/1230983e-f85c-49e6-a32c-58cf1bf8eb29)

# Usage

In your shell, `cd` to the directory containing `pyloc` and then do
```
./pyloc projectdir
```
where `projectdir` is the path to your project directory. For example `./pyloc ~/Desktop/clones/pandas`. The result is the sum of all true Python lines of code across all .py files in `projectdir`. You can also use `pyloc` on a single file e.g. `./pyloc ~/my_amazing_script.py`.

You can optionally specify a pattern to match filenames with the `-p` option. For example,
```
./pyloc ~/Desktop/clones/pandas -p "test_*.py"
```
prints the true number of lines of Python code in all the test files.

Other options:
```
./pyloc ~/Desktop/clones/pandas -a
```
prints the lines of code in each .py file, along with the total across all files.

```
./pyloc ~/Desktop/clones/pandas -s
```
prints the statistics (mean, median and max) of lines of code, along with the total across all files.

You can also combine options, for example,
```
./pyloc ~/Desktop/clones/pandas -sa -p "test_*.py"
```

![pandas_sa](https://github.com/user-attachments/assets/43853751-6409-40cc-91c3-2321277b5be6)

Make sure `pyloc` has executable permissions. If not, do `chmod +x ./pyloc` in your terminal.

To use `pyloc` directly like a command in your terminal, add it to your PATH. For example, for zsh users: to the configuration file `~/.zshrc`, add the line 
`export PATH=$PATH:~/.local/bin`, create the directories with `mkdir ~/.local` and `mkdir ~/.local/bin`, and then do `cp ./pyloc ~/.local/bin/pyloc`.

You can now just `cd` to the project directory you are interested in and simply do
```
pyloc .
```

Terminal sessions recorded and GIFs created using [asciinema](https://github.com/asciinema).
