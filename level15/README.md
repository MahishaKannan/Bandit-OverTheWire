-

# Level 15 — `README.md`

Your second screenshot shows the important part of Level 15: using `ncat` with SSL on port `30001`.

Copy-paste this into `Level-15/README.md`:

```markdown
# Bandit Level 15

## Objective

Connect to the local service using SSL and obtain the password for the next level.

## Steps

1. I logged in to the Bandit Level 15 account.
2. I used the following command to connect to the local SSL service:

```bash
ncat --ssl localhost 30001
The service was successfully connected.
I entered the password obtained from the previous level.
The service returned the required password for the next level.
I exited the Bandit session using:
exit
Result

Successfully connected to the SSL service on port 30001 and obtained the password for the next level.

What I Learned

I learned how to use ncat to connect to a local service using an SSL connection