---

# LEVEL 11 — `README.md`

```markdown
# Bandit Level 11

## Objective

Decode the password stored in `data.txt`.

## Steps

1. Log in to the Bandit Level 11 account.
2. Enter the password from Level 10.
3. Open `data.txt`.
4. Identify that the text is encoded using ROT13.
5. Decode the text.
6. Obtain the password for the next level.

## Command Used

```bash
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
Result

The ROT13 encoded text was decoded and the password was obtained.

What I Learned

I learned about ROT13 and how the tr command can be used for character substitution.