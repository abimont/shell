# Shell: I/O, Redirections and Filters

This project was developed as part of the Holberton School training. Each file in this directory contains the answer corresponding to an exercise, and explores Shell's input/output redirections, or how, by using some special notations we can redirect the output of many commands to files, devices, and even to the input of other commands. But, how?

### Standard output

By default, standard output directs its contents to the display. To redirect standard output to a file, the ">" character is used like this:

```
$ ls > file.txt
```

In this example, the ls command is executed and the results are written in a file named file.txt. Each time this command is repeated, file.txt is overwritten. To have the new results appended to the file instead, we use ">>" like this:

```
$ls >> file.txt
```

When the results are appended, the new results are added to the end of the file. If the file does not exist, will be created.

### Standard Input

Many commands can accept input from a facility called standard input. By default, standard input gets its contents from the keyboard, but like standard output, it can be redirected. To redirect standard input from a file instead of the keyboard, the "<" character is used like this:

```
$ sort < file.txt
```

In this example, we used the sort command to process the contents of file.txt. The results are output on the display since the standard output was not redirected. We could redirect standard output by using it with output redirection.

### Pipelines

The most useful and powerful thing we can do with I/O redirection is to connect multiple commands together to form what are called pipelines. With pipelines, the standard output of one command is fed into the standard input of another. Here is a very useful example:

```
$ ls -l | less
```

In this example, the output of the ls command is fed into less. By using this "| less" trick, we can make any command have scrolling output.

## Filters

One kind of program frequently used in pipelines is called a filter. Filters take standard input and perform an operation upon it and send the results to standard output. In this way, they can be combined to process information in powerful ways. Here are some of the common programs that can act as filters:

- `sort`:	Sorts standard input then outputs the sorted result on standard output.
- `uniq`:	Given a sorted stream of data from standard input, it removes duplicate lines of data (i.e., it makes sure that every line is unique).
- `grep`:	Examines each line of data it receives from standard input and outputs every line that contains a specified pattern of characters.
- `fmt`:	Reads text from standard input, then outputs formatted text on standard output.
- `pr`:	Takes text input from standard input and splits the data into pages with page breaks, headers and footers in preparation for printing.
- `head`:	Outputs the first few lines of its input. Useful for getting the header of a file.
- `tail`:	Outputs the last few lines of its input. Useful for things like getting the most recent entries from a log file.
- `tr`:	Translates characters. Can be used to perform tasks such as upper/lowercase conversions or changing line termination characters from one type to another (for example, converting DOS text files into Unix style text files).
- `sed`:	Stream editor. Can perform more sophisticated text translations than tr.
- `awk`:	An entire programming language designed for constructing filters. Extremely powerful.
