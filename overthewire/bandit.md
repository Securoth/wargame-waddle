# Bandit

## Level 0: Printing File Contents

This level requires reading the contents of a text file. Without a graphical text editor like Notepad++, a command line user will need to be able to view the contents of these files directly within their terminal.

The cat command provides an easy way to view text files. The syntax is very simple: `cat [options] [file(s)]` . In most cases, no options will be needed.

So, to get the password we simply run the following:

```bash
cat readme
```

### Further Exploration

`cat`, along with many of the basic commands used in Bandit, are part of the GNU coreutils package. This means you will find them on almost every Linux and Unix System. To read more about the GNU organization and their role in developing and promoting free and open source \(FOSS\) software, check out the [About GNU](https://www.gnu.org/gnu/thegnuproject.en.html) section of their website.

## Level 1: Reading Irregularly Named File

At first glance, this looks identical to level 0 only with a different file name. However, trying to run the command with `-` as the filename will instead cause it to wait for you to give input then display what you just typed. This behavior will continue until you kill the command with CTRL+c

In \*nix, many utilities interpret a `-` as a request to take input from the standard input stream\(keyboard\) instead of a file. In order to read the file, it will have to be specified using its path. This will prevent the filename from being interpreted as the standard input flag.

### Solution 1: Specify the File Path

The easiest method is to use the relative path, which is the location of the file relative to the current directory. Assuming you are in the starting directory /home/bandit1, you would specify the relative path like so:

```bash
cat ./-
```

The absolute path would work as well. Absolute paths are longer to type but don't have any reference to the current directory. Instead, they tell you where the file is starting at the root of the system. If you use an absolute path the meaning will always be the same, no matter which directory you happen to be working in.

```bash
cat /home/bandit1/-
```

### Solution 2: File Redirection

Another valid option is using a file redirection operator. The use of &lt; on the command line indicates that the program on the left side of the operator should read in the data from the input on right side. This operator is not normally needed with the cat command, which reads from a file by default, but not every command behaves this way. Even though its use with cat is redundant, it has one big advantage; it doesn't interpret `-` to mean anything, so it will treat it like a normal filename.

```bash
cat < -
```

### Further Exploration

Linux doesn't place restrictions on what you can name a file. [Almost any character](https://unix.stackexchange.com/questions/230291/what-characters-are-valid-to-use-in-filenames) can be used a file name. However, many allowable names will cause difficulty for other programs interacting with your file. Follow a few simple rules:

* DONT start file names with a -, which is usually interpreted as the start of a command line switch
* DONT use symbols that may be interpreted by BASH such as % or $
* DONT use spaces, uses dashes or underscores instead

## Level 2: Reading a File with Spaces in the Name



