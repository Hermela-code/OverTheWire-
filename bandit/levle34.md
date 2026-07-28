# Bandit Level 3 → Level 4 Write-Up

After logging in with the password from **Bandit Level 3**, the goal is to find the password for **Level 4**.

According to the hint, the password is stored in a **hidden file** inside the `inhere` directory.

## Step 1: Check the current directory

First, list the files in the home directory:

```bash
ls
```

Output:

```text
inhere
```

![level340](images/level340.png)

We can see a directory named `inhere`.

## Step 2: Enter the directory

Move into the `inhere` directory:

```bash
cd inhere
```

Now, list the files:

```bash
ls
```

No files are displayed.

This happens because `ls` does not show hidden files by default.

## Step 3: Show hidden files

To display hidden files, use the `-a` option:

```bash
ls -a
```

Output:

```text
.  ..  ...Hiding-From-You
```

Explanation:

* `.` refers to the current directory.
* `..` refers to the parent directory.
* `...Hiding-From-You` is the hidden file containing the password.

## Step 4: Read the hidden file

Use `cat` to display the file contents:

```bash
cat ./...Hiding-From-You
```

The `./` refers to the current directory and ensures that Linux treats `...Hiding-From-You` as a filename.

This command reveals the password for **Bandit Level 4**.

![level342](images/level342.png)



## What I Learned

* Hidden files in Linux start with `.`.
* `ls` does not display hidden files by default.
* `ls -a` shows all files, including hidden ones.
* `.` represents the current directory.
* `..` represents the parent directory.
* `cat` is used to read file contents.

```
```
<details>
<summary> Click here to see the password </summary>
xzTXq1rDJQVVAzdv5cHq1TQytTWufAMq
</details>
