# OverTheWire Bandit Write-up

Here you can find the write up for the OverTheWire Bandit game.  
This game helps you learn the basics of the Linux command-line interface in a fun way and consists of 35 levels.

## Level0 Game Descritpion

<img width="1920" height="1080" alt="s1" src="https://github.com/user-attachments/assets/65dea29a-10da-4a51-bd4c-9f40d4764d0b" />
So, as you read from the game description, the goal of the game is to get information such as the password from the previous level to enter the next level. So, let’s begin with Level 0.

![od](https://github.com/user-attachments/assets/9e9d664d-6612-4d93-9684-45ab2bd8ce71)

## Solution with explanation

The main thing you need to know to solve this problem is **SSH (Secure Shell)**. SSH is a protocol that lets you securely connect to a remote computer's command line.

Use this command:
```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
```
It will prompt you for a password. Enter the password you obtained from the level 0 description ``` bash bandit0```. Congratulations, now you have access to bandit shell.

![0s](https://github.com/user-attachments/assets/0878412f-70c0-48e8-ae4c-28c4e41df0f9)

## Bandit Level 0 → Level 1 Descritpion

![1d](https://github.com/user-attachments/assets/ae9f7980-95fd-4fee-b4ff-7bdc11541839)
To get from Level 0 to Level 1 we need to find the password in the Level 0 bandit shell. As the description shows, it is stored in the `readme` file. We can check whether the file is there using `ls`, which lists files and folders. Then use `cat readme` to display the password needed for Level 1.
<details>
  <summary> Click here to reveal the password</summary>

  **Password:** `ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If`
</details>

