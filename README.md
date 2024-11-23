# Advent of Code
This is a C# repository template for your [Advent of Code](https://adventofcode.com) solutions. I've been using this since 2015
with [great success](https://github.com/encse/adventofcode). 

![](demo.gif)

It's not a command line tool, but rather a batteries included framework that does the heavy lifting. While you focus on solving the problems it provides:

- input download
- a solution skeleton generator
- online answer validation
- regression tests
- speed tests
- up to date calendar in ANSI colors for the terminal, as well as an SVG version for your README.md
- source lines of code (sloc) chart
- an OCR for elf fonts.

Due to copyright reasons I'm not allowed to include input files and problem descriptions
within this repository. But I wanted to have a self contained version for myself that I can keep around forever, 
so decided to commit the encrypted version of the input files. It doesn't violate the 
copyright since it's just random garbage for everyone else but when I check it out, a plugin 
called `git-crypt` decrypts all my inputs transparently, so that I can work with them uninterrupted.
 
On commit the whole process is reversed and the files get encrypted again.

## Dependencies

- Based on `.NET 9` and `C# 13` 
- `AngleSharp` is used for problem download
- `git-crypt` to store the input files in an encrypted form
- the optional `Memento Inputs` extension for Visual Studio Code

## Getting started in 5 steps

1. Clone the repo
2. Install .NET
3. Install and initialize git-crypt:

```
> brew install git-crypt
> cd repo-dir
> git-crypt init
> git-crypt export-key ~/aoc-crypt.key
```

Don't commit `aoc-crypt.key` into a public repo, back it up in some protected place. 
If you need to clone your repo later you will need to unlock it using this key such as:

```
> git clone ...
> cd repo-dir
> git-crypt unlock ~/aoc-crypt.key
```
4. export your SESSION cookie from the adventofcode.com site in your terminal as an env variable:

```
> export SESSION=djsaksjakshkja...
```

5. Get help with `dotnet run` and start coding.

## Working in Visual Studio Code
If you prefer, you can work directly in VSCode as well. 

Open the command Palette (⇧ ⌘ P), select `Tasks: Run Task` then e.g. `update today`.

Work on part 1. Check the solution with the `upload today` task. Continue with part 2.

**Note:** this feature relies on the "Memento Inputs" extension to store your session cookie, you need 
to set it up in advance from the Command Palette with `Install Extensions`.
