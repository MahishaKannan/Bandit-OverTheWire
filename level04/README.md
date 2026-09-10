---

# LEVEL 04 — `README.md`

```markdown
# Bandit Level 04

## Objective

Find the file containing readable text inside the `inhere` directory.

## Steps

1. Change to the Bandit Level 4 account.
2. Enter the password obtained from the previous level.
3. Go to the `inhere` directory.
4. List the files.
5. Check the type of the files.
6. Identify the file containing readable text.
7. Read the file using the `cat` command.

## Commands Used

```bash
cd inhere
ls
file ./*
cat ./-file07
Result

The readable file was identified and its contents provided the password for the next level.

What I Learned

I learned how the file command can be used to identify the type of files.