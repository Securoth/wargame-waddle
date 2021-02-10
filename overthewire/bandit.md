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

At first glance, this looks identical to level 0 only but with a different file name. However, trying to run the command with `-` as the filename will instead cause it to wait for you to give input then display what you just typed. This behavior continue until you kill the command with CTRL+c

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



### Further Exploration



## Level 2: 

