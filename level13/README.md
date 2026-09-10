---

# LEVEL 13 — `README.md`

```markdown
# Bandit Level 13

## Objective

Use the SSH private key provided in the previous level to log in to the next Bandit account.

## Steps

1. Log in to the Bandit Level 13 account.
2. Enter the password obtained from Level 12.
3. List the files in the current directory.
4. Identify the SSH private key.
5. Use the private key to connect to the next Bandit account.
6. Successfully log in using the key.

## Commands Used

```bash
ls
ssh -i <private-key-file> bandit14@localhost -p 2220
Result

The SSH private key was used successfully to connect to the next level.

What I Learned

I learned how SSH private keys can be used for authentication instead of entering a password.