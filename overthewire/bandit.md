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

At first glance, this looks identical to level 0 only but with a different file name. However, trying to run the command with - as the filename will instead cause it to wait for you to give additional input and then display what you just typed. This behavior can be observed below:



