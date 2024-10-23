# Advent of Code
C# solutions to the [Advent of Code](https://adventofcode.com) problems.

This is a repository template to be used as a baseline in your own 'adventures'.
It's a batteries included framework that can download your inputs, scaffold a solution template, 
send in and validate your answers, generate svg versions of your calendar as you progress etc.
I've been using this since 2015 with [great success](https://github.com/encse/adventofcode).

Due to copyright requirements I'm not allowed to include input files and problem descriptions
within this repository. 

However I wanted to have a self contained version for myself that I can keep around forever, 
so I decided to commit the encrypted version of the input files. It doesn't violate the 
copyright since it's just random garbage for everyone else but when I check it out, a plugin 
called `git-crypt` decrypts all my inputs transparently, so I can work with them uninterrupted.
 
On commit the whole process is reversed and the files get encrypted again.

If you find this project useful, please [support](https://github.com/sponsors/encse) me.

## Dependencies

- Based on `.NET 8` and `C# 12` 
- `AngleSharp` is used for problem download
- `git-crypt` to store the input files in an encrypted form
- the optional `Memento Inputs` extension for Visual Studio Code

## Getting started

1. Clone the repo
2. Install .NET Core
3. Install and initialize git-crypt:

```
> brew install git-crypt
> cd repo-dir
> git-crypt init
> git-crypt export-key ~/aoc-crypt.key
```

4. Don't commit `aoc-crypt.key` into a public repo, back it up in some protected place. 
If you need to clone your repo later you will need to unlock it using this key such as:

```
> git clone ...
> cd repo-dir
> git-crypt unlock ~/aoc-crypt.key
```

5. Get help with `dotnet run` and start coding.

## Working in Visual Studio Code
If you prefer, you can work directly in VSCode as well. 

Open the command Palette (⇧ ⌘ P), select `Tasks: Run Task` then e.g. `update today`.

Work on part 1. Check the solution with the `upload today` task. Continue with part 2.

**Note:** this feature relies on the "Memento Inputs" extension to store your session cookie, you need 
to set it up in advance from the Command Palette with `Install Extensions`.
