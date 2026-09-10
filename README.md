
# OverTheWire Bandit – Level 0 to Level 15

## About

This repository contains my practical learning journey through the
OverTheWire Bandit challenge.

I completed the levels from Level 0 to Level 15 and documented the
commands, steps, results and concepts I learned.

Each level is supported by a terminal screenshot showing my practical work.

---

# Level 00

## Objective

Connect to the Bandit server using SSH.

## Command Used

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
````

## Steps

1. Opened the terminal.
2. Used SSH to connect to the Bandit server.
3. Used port 2220.
4. Entered the required password.
5. Successfully connected to the Bandit environment.

## Result

Successfully completed Level 00.

## What I Learned

I learned how SSH is used to connect to a remote Linux system.

## Terminal Screenshot

![Level 00](Level-00.png)

---

# Level 01

## Objective

Read the required file and obtain the information needed for the next level.

## Commands Used

```bash
ls
cat readme
```

## Steps

1. Listed the files in the directory.
2. Found the `readme` file.
3. Used the `cat` command to display the contents.
4. Obtained the required information.

## Result

Successfully completed Level 01.

## What I Learned

I learned how to list files and read file contents using Linux commands.

## Terminal Screenshot

![Level 01](Level-01.png)

---

# Level 02

## Objective

Read a file whose name contains spaces.

## Steps

1. Listed the files in the directory.
2. Identified the file containing spaces in its name.
3. Used the filename correctly with the `cat` command.
4. Read the required information.

## Command

```bash
cat "spaces in this filename"
```

## Result

Successfully read the file and obtained the required information.

## What I Learned

I learned how Linux handles filenames containing spaces.

## Terminal Screenshot

![Level 02](Level-02.png)

---

# Level 03

## Objective

Find and read a hidden file.

## Steps

1. Entered the required directory.
2. Used the `ls -a` command to display hidden files.
3. Identified the hidden file.
4. Read the contents of the hidden file.

## Commands

```bash
cd inhere
ls -a
cat .hidden
```

## Result

The hidden file was found and the required information was obtained.

## What I Learned

I learned how to identify hidden files in Linux.

## Terminal Screenshot

![Level 03](Level-03.png)

---

# Level 04

## Objective

Find the readable file among the files in the directory.

## Steps

1. Entered the `inhere` directory.
2. Listed the files.
3. Used the `file` command to identify the file types.
4. Found the readable file.
5. Read its contents.

## Commands

```bash
cd inhere
ls
file ./*
```

## Result

The readable file was identified and the required information was obtained.

## What I Learned

I learned how the `file` command can be used to identify file types.

## Terminal Screenshot

![Level 04](Level-04.png)

---

# Level 05

## Objective

Find the required file based on its properties.

## Steps

1. Entered the required directory.
2. Searched for files.
3. Checked the file properties.
4. Identified the required file.
5. Read the file contents.

## Command

```bash
find inhere -type f
```

## Result

The required file was found successfully.

## What I Learned

I learned how the `find` command can be used to search for files.

## Terminal Screenshot

![Level 05](Level-05.png)

---

# Level 06

## Objective

Find a file located somewhere in the system based on its properties.

## Steps

1. Searched the system for the required file.
2. Used file properties to narrow down the search.
3. Ignored permission-error messages where necessary.
4. Identified the required file.
5. Read its contents.

## Command

```bash
find / -type f -size 33c 2>/dev/null
```

## Result

The required file was found successfully.

## What I Learned

I learned how to search the Linux filesystem using file properties.

## Terminal Screenshot

![Level 06](Level-06.png)

---

# Level 07

## Objective

Find the required information inside `data.txt`.

## Steps

1. Opened the `data.txt` file.
2. Searched for the required word.
3. Used `grep` to find the matching line.
4. Obtained the required information.

## Command

```bash
grep "millionth" data.txt
```

## Result

The required information was found inside `data.txt`.

## What I Learned

I learned how `grep` can be used to search for specific text inside a file.

## Terminal Screenshot

![Level 07](Level-07.png)

---

# Level 08

## Objective

Find the unique line in `data.txt`.

## Steps

1. Checked the contents of the file.
2. Sorted the lines.
3. Used `uniq` to identify the line that occurs only once.
4. Obtained the required information.

## Command

```bash
sort data.txt | uniq -u
```

## Result

The unique line was identified successfully.

## What I Learned

I learned how `sort` and `uniq` can be combined to find unique lines.

## Terminal Screenshot

![Level 08](Level-08.png)

---

# Level 09

## Objective

Find human-readable information inside the data file.

## Steps

1. Checked the data file.
2. Used the `strings` command.
3. Identified readable text.
4. Located the required information.

## Commands

```bash
strings data.txt
```

## Result

The required human-readable information was identified.

## What I Learned

I learned how the `strings` command can extract readable text from a file.

## Terminal Screenshot

![Level 09](Level-09.png)

---

# Level 10

## Objective

Decode the encoded contents of `data.txt`.

## Steps

1. Checked the contents of `data.txt`.
2. Identified that the data was Base64 encoded.
3. Used the Base64 decoding command.
4. Obtained the required information.

## Commands

```bash
cat data.txt
base64 -d data.txt
```

## Result

The Base64 encoded data was decoded successfully.

## What I Learned

I learned about Base64 encoding and how to decode it using Linux.

## Terminal Screenshot

![Level 10](Level-10.png)

---

# Level 11

## Objective

Decode the text using ROT13.

## Steps

1. Opened `data.txt`.
2. Identified that the text was encoded using ROT13.
3. Used character translation to decode the text.
4. Obtained the required information.

## Command

```bash
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```

## Result

The ROT13 encoded text was decoded successfully.

## What I Learned

I learned about ROT13 and how the `tr` command can be used for character substitution.

## Terminal Screenshot

![Level 11](Level-11.png)

---

# Level 12

## Objective

Extract the required information from a file that has been compressed multiple times.

## Steps

1. Created a temporary working directory.
2. Copied the data file into the temporary directory.
3. Checked the file type.
4. Renamed the file according to its compression format.
5. Decompressed the file.
6. Repeated the process for the different compression layers.
7. Finally obtained the required information.

## Commands Used

```bash
mkdir /tmp/<directory-name>
cp data.txt /tmp/<directory-name>
cd /tmp/<directory-name>
file data.txt
```

The file was repeatedly identified, renamed and decompressed according to its type.

## Result

The different compression layers were successfully extracted.

## What I Learned

I learned how to identify different file types and extract compressed files step-by-step.

## Terminal Screenshot

![Level 12](Level-12.png)

---

# Level 13

## Objective

Use the SSH private key to connect to the next Bandit account.

## Steps

1. Logged in to the Bandit Level 13 account.
2. Listed the files.
3. Identified the SSH private key.
4. Used the private key for authentication.
5. Connected to the next Bandit account.

## Command

```bash
ssh -i <private-key-file> bandit14@localhost -p 2220
```

## Result

Successfully used the SSH private key to connect to the next level.

## What I Learned

I learned how SSH private keys can be used for authentication.

## Terminal Screenshot

![Level 13](Level-13.png)

---

# Level 14

## Objective

Read the password for Bandit Level 14 and use it to continue to the next level.

## Steps

1. I was logged in to the Bandit Level 14 account.
2. I read the password file using:

```bash
cat /etc/bandit_pass/bandit14
```

3. The password was displayed in the terminal.
4. I exited the current session using:

```bash
exit
```

5. From my local PowerShell terminal, I connected to Bandit Level 15 using:

```bash
ssh bandit15@bandit.labs.overthewire.org -p 2220
```

6. The Bandit login screen was displayed successfully.

## Result

Successfully connected to the Bandit Level 15 account.

## What I Learned

I learned how to read a password file and use the obtained credentials to connect to the next Bandit level using SSH.

## Terminal Screenshot

![Level 14](Level-14.png)

---

# Level 15

## Objective

Connect to the local service using an SSL connection.

## Steps

1. Logged in to the Bandit Level 15 account.
2. Connected to the local SSL service.
3. Used port `30001`.
4. Entered the password obtained from the previous level.
5. The service returned `Correct!`.
6. The required information for continuing the challenge was obtained.
7. Exited the Bandit session.

## Command Used

```bash
ncat --ssl localhost 30001
```

## Result

The SSL connection was successful and the service responded with:

```text
Correct!
```

## What I Learned

I learned how `ncat` can be used to connect to a local service using SSL.

I also learned the importance of ports and secure network connections.

## Terminal Screenshot

![Level 15](Level-15.png)

---

# Overall Learning

Through the Bandit challenge, I practiced several Linux and cybersecurity concepts.

## Linux Skills

* SSH
* File and directory navigation
* Reading files
* Hidden files
* File searching
* File identification
* Text searching
* File compression

## Cybersecurity Skills

* Remote authentication
* Password-based authentication
* SSH private keys
* Encoding and decoding
* ROT13
* Base64
* SSL connections
* Network ports
* Basic command-line security

## Commands Practiced

```text
ssh
ls
cd
cat
ls -a
file
find
grep
sort
uniq
strings
base64
tr
mkdir
cp
exit
ncat
```

# Conclusion

The OverTheWire Bandit challenge helped me improve my Linux command-line skills and understand practical cybersecurity concepts.

Completing Level 0 to Level 15 gave me hands-on experience with file handling, searching, encoding, compression, SSH authentication and basic network services.

The terminal screenshots included in this repository provide evidence of my practical work.

````


**Also, don't put the actual passwords from your screenshots into the README.** The screenshots are enough evidence, and hiding the passwords makes the GitHub repository safer to share publicly.
