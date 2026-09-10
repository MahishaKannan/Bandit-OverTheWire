
---

# LEVEL 12 — `README.md`

```markdown
# Bandit Level 12

## Objective

Extract the password from a file that has been compressed multiple times.

## Steps

1. Log in to the Bandit Level 12 account.
2. Enter the password from Level 11.
3. Check the `data.txt` file.
4. Create a temporary working directory.
5. Copy the file into the temporary directory.
6. Identify the file type.
7. Rename the file according to its compression format.
8. Decompress the file.
9. Repeat the process until the human-readable password is obtained.

## Commands Used

```bash
mkdir /tmp/<directory-name>
cp data.txt /tmp/<directory-name>
cd /tmp/<directory-name>
file data.txt

The file was repeatedly renamed and decompressed according to its file type.

Result

After extracting the different compressed layers, the password for the next level was obtained.

What I Learned

I learned how to identify compressed files and extract files step-by-step.