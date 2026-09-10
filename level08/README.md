---

# LEVEL 08 — `README.md`

```markdown
# Bandit Level 08

## Objective

Find the unique line in `data.txt`.

## Steps

1. Log in to the Bandit Level 8 account.
2. Enter the password obtained from Level 7.
3. Check the `data.txt` file.
4. Count the lines in the file.
5. Find the line that occurs only once.
6. Obtain the password for the next level.

## Commands Used

```bash
ls
wc -l data.txt
sort data.txt | uniq -u
Result

The unique line was identified and it contained the password for the next level.

What I Learned

I learned how sort and uniq can be used together to find unique lines.