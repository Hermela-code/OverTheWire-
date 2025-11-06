# OverTheWire Bandit Write-up

Here you can find the write up for the OverTheWire Bandit game.  
This game helps you learn the basics of the Linux command-line interface in a fun way and consists of 35 levels.

## Game Descritpion

<img width="1920" height="1080" alt="s1" src="https://github.com/user-attachments/assets/65dea29a-10da-4a51-bd4c-9f40d4764d0b" />
So, as you read from the game description, the goal of the game is to get information such as the password from the previous level to enter the next level. So, let’s begin with Level 0.

![od](https://github.com/user-attachments/assets/9e9d664d-6612-4d93-9684-45ab2bd8ce71)

## Solution with explanation

The main thing you need to know to solve this problem is **SSH (Secure Shell)**. SSH is a protocol that lets you securely connect to a remote computer's command line.

Use this command:
```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
```
It will prompt you for a password. Enter the password you obtained from the previous level (for example: bandit0). Congratulations, now you have access to bandit shell
