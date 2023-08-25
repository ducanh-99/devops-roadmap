<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

- [Bash](#bash)
  - [Execute the bash scripts](#execute-the-bash-scripts)
  - [Looping and Branching in Bash](#looping-and-branching-in-bash)
  - [How to Schedule Scripts using cron](#how-to-schedule-scripts-using-cron)
  - [How to Debug and Troubleshoot Bash Scripts](#how-to-debug-and-troubleshoot-bash-scripts)
    - [Set the set -x option](#set-the-set--x-option)

<!-- /code_chunk_output -->

# Bash

```bash
command [Option] arguments
```

`date`: Displays the current date

```
date
```

`pwd`: Displays the present working directory.

`ls`: Lists the contents of the current directory.

`echo`: Prints a string of text, or value of a variable to the terminal.

You can always refer to a commands manual with the `man` command.

For example, the manual for `ls` looks something like this:

```
man ls
```

## Execute the bash scripts

assign execution rights to your user using this command

```bash
chmod u+x run_all.sh
```

run file

```bash
sh run_all.sh
bash run_all.sh
./run_all.sh
```

## Looping and Branching in Bash

```bash
#!/bin/bash
i=1
while [[ $i -le 10 ]] ; do
   echo "$i"
  (( i += 1 ))
done
```

## How to Schedule Scripts using cron

Below is the syntax to schedule crons:

```bash
# Cron job example
* * * * * sh /path/to/script.sh
```

to list all crontab

```bash 
crontab -l
```


## How to Debug and Troubleshoot Bash Scripts

### Set the set -x option

```bash
#!/bin/bash

set -x

# Your script goes here
```
