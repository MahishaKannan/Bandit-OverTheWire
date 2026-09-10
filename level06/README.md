---

# LEVEL 06 — `README.md`

```markdown
# Bandit Level 06

## Objective

Find a file that has the required properties and contains the password.

## Steps

1. Change to the Bandit Level 6 account.
2. Enter the password from the previous level.
3. Search for the required file.
4. Use the file properties such as size and permissions to identify it.
5. Read the identified file.
6. Obtain the password for the next level.

## Command Used

```bash
find / -type f -size 33c 2>/dev/null
Result

The required file was found and its contents provided the password.

What I Learned

I learned how to search for files using properties such as file type and size.