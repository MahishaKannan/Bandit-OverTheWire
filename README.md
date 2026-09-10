# OverTheWire Bandit – Level 0 to Level 15

## About

This repository contains my practical learning journey through the OverTheWire Bandit challenge.

I have documented my work from Level 0 to Level 15 with the commands used, steps followed, results obtained, and the concepts I learned.

The purpose of this repository is to record my practical Linux and cybersecurity learning and to provide a simple reference for beginners.

---

# Level 00

## Objective

Connect to the Bandit server using SSH.

## Command Used

ssh bandit0@bandit.labs.overthewire.org -p 2220

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

---

# Level 01

## Objective

Read the required file to obtain the information needed for the next level.

## Commands Used

ls

cat readme

## Steps

1. Listed the files in the current directory.
2. Found the readme file.
3. Used the cat command to display its contents.
4. Obtained the required information.

## Result

Successfully completed Level 01.

## What I Learned

I learned how to list files and read the contents of a file using Linux commands.

---

# Level 02

## Objective

Read a file whose filename contains spaces.

## Steps

1. Listed the files in the directory.
2. Identified the file containing spaces in its name.
3. Used the filename correctly with the cat command.
4. Read the required information.

## Command Used

cat "filename with spaces"

## Result

Successfully read the file and obtained the required information.

## What I Learned

I learned how to work with filenames that contain spaces in Linux.

---

# Level 03

## Objective

Find and read a hidden file inside the required directory.

## Steps

1. Entered the required directory.
2. Used the ls -a command to display hidden files.
3. Identified the required hidden file.
4. Read the contents of the hidden file.
5. Obtained the required information.

## Commands Used

cd inhere

ls -a

cat .hidden

## Result

The hidden file was found and the required information was obtained.

## What I Learned

I learned how hidden files can be displayed and accessed in Linux.

---

# Level 04

## Objective

Find the readable file among the files in the directory.

## Steps

1. Entered the inhere directory.
2. Listed the files.
3. Checked the file types.
4. Identified the readable file.
5. Read the contents of the file.

## Commands Used

cd inhere

ls

file ./*

## Result

The readable file was identified and the required information was obtained.

## What I Learned

I learned how the file command can be used to identify the type of a file.

---

# Level 05

## Objective

Find the required file based on its properties.

## Steps

1. Entered the required directory.
2. Searched for files.
3. Checked the properties of the files.
4. Identified the required file.
5. Read the file contents.

## Command Used

find inhere -type f

## Result

The required file was found successfully.

## What I Learned

I learned how the find command can be used to search for files.

---

# Level 06

## Objective

Find the required file somewhere in the system based on its properties.

## Steps

1. Searched the filesystem for the required file.
2. Used file properties to narrow down the search.
3. Ignored permission-error messages where necessary.
4. Identified the required file.
5. Read its contents.

## Command Used

find / -type f -size 33c 2>/dev/null

## Result

The required file was found successfully.

## What I Learned

I learned how to search the Linux filesystem using file properties.

---

# Level 07

## Objective

Find the required information inside the data.txt file.

## Steps

1. Checked the data.txt file.
2. Searched for the required word.
3. Used grep to find the matching line.
4. Obtained the required information.

## Command Used

grep "millionth" data.txt

## Result

The required information was found inside data.txt.

## What I Learned

I learned how grep can be used to search for specific text inside a file.

---

# Level 08

## Objective

Find the unique line in data.txt.

## Steps

1. Checked the contents of the file.
2. Sorted the lines.
3. Used uniq to identify the line that occurs only once.
4. Obtained the required information.

## Command Used

sort data.txt | uniq -u

## Result

The unique line was identified successfully.

## What I Learned

I learned how sort and uniq can be combined to find unique lines.

---

# Level 09

## Objective

Find human-readable information inside the data file.

## Steps

1. Checked the data file.
2. Used the strings command.
3. Identified readable text.
4. Located the required information.

## Command Used

strings data.txt

## Result

The required human-readable information was identified.

## What I Learned

I learned how the strings command can be used to extract readable text from a file.

---

# Level 10

## Objective

Decode the encoded contents of data.txt.

## Steps

1. Checked the contents of data.txt.
2. Identified that the data was Base64 encoded.
3. Used the Base64 decoding command.
4. Obtained the required information.

## Commands Used

cat data.txt

base64 -d data.txt

## Result

The Base64 encoded data was decoded successfully.

## What I Learned

I learned about Base64 encoding and how to decode Base64 data using Linux.

---

# Level 11

## Objective

Decode the text using ROT13.

## Steps

1. Opened data.txt.
2. Identified that the text was encoded using ROT13.
3. Used character translation to decode the text.
4. Obtained the required information.

## Command Used

cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'

## Result

The ROT13 encoded text was decoded successfully.

## What I Learned

I learned about ROT13 and how the tr command can be used for character substitution.

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

mkdir /tmp/<directory-name>

cp data.txt /tmp/<directory-name>

cd /tmp/<directory-name>

file data.txt

## Result

The different compression layers were successfully extracted.

## What I Learned

I learned how to identify different file types and extract compressed files step-by-step.

---

# Level 13

## Objective

Use the SSH private key to connect to the next Bandit account.

## Steps

1. Logged in to the Bandit Level 13 account.
2. Listed the files in the directory.
3. Identified the SSH private key.
4. Used the private key for authentication.
5. Connected to the next Bandit account.

## Command Used

ssh -i <private-key-file> bandit14@localhost -p 2220

## Result

Successfully used the SSH private key to connect to the next level.

## What I Learned

I learned how SSH private keys can be used for authentication.

---

# Level 14

## Objective

Read the password for Bandit Level 14 and use it to continue to the next level.

## Steps

1. Logged in to the Bandit Level 14 account.
2. Read the password file.
3. The password was displayed in the terminal.
4. Exited the current session.
5. Connected to Bandit Level 15 using SSH.

## Commands Used

cat /etc/bandit_pass/bandit14

exit

ssh bandit15@bandit.labs.overthewire.org -p 2220

## Result

Successfully connected to the Bandit Level 15 account.

## What I Learned

I learned how to read a password file and use the obtained credentials to connect to the next Bandit level using SSH.

---

# Level 15

## Objective

Connect to the local service using an SSL connection.

## Steps

1. Logged in to the Bandit Level 15 account.
2. Connected to the local SSL service.
3. Used port 30001.
4. Entered the password obtained from the previous level.
5. The service responded with "Correct!".
6. Successfully completed the connection.

## Command Used

ncat --ssl localhost 30001

## Result

The SSL connection was successful and the service responded with:

Correct!

## What I Learned

I learned how ncat can be used to connect to a local service using SSL.

I also learned about using network ports and secure network connections.

---

# Overall Learning

Through the OverTheWire Bandit challenge, I practiced several Linux and cybersecurity concepts.

## Linux Skills

- SSH
- File and directory navigation
- Reading files
- Hidden files
- Searching files
- File identification
- Text searching
- File compression
- Command-line operations

## Cybersecurity Skills

- Remote authentication
- Password-based authentication
- SSH private keys
- Encoding and decoding
- Base64
- ROT13
- SSL connections
- Network ports
- Basic command-line security

## Commands Practiced

- ssh
- ls
- cd
- cat
- ls -a
- file
- find
- grep
- sort
- uniq
- strings
- base64
- tr
- mkdir
- cp
- exit
- ncat

# Conclusion

The OverTheWire Bandit challenge helped me improve my Linux command-line skills and understand practical cybersecurity concepts.

By completing Level 0 to Level 15, I gained hands-on experience with file handling, searching, encoding, compression, SSH authentication and basic network services.

This repository documents my practical learning journey and can also serve as a simple reference for beginners learning Linux and cybersecurity.
