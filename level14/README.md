# Bandit Level 14

## Objective

Obtain the password for Bandit Level 14 and use it to connect to Bandit Level 15.

## Steps

1. I was logged in to the Bandit Level 14 account.
2. I used the following command to read the password file:

```bash
cat /etc/bandit_pass/bandit14
The password for Bandit Level 14 was displayed in the terminal.
I exited the current Bandit session using:
exit
From my local PowerShell terminal, I connected to Bandit Level 15 using SSH:
ssh bandit15@bandit.labs.overthewire.org -p 2220
The Bandit Level 15 login screen was displayed successfully.
Result

Successfully connected to the Bandit Level 15 account.

What I Learned

I learned how to read a password file and use the obtained credentials to connect to the next Bandit level using SSH.