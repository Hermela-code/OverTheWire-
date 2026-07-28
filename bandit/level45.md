# Bandit Level 4 → Level 5 Write-Up

After logging in with the password from **Bandit Level 4**, the goal is to find the password for **Level 5**.

According to the hint, the password is stored in the **only human-readable file** inside the `inhere` directory.

## Step 1: Check the current directory

First, list the files in the home directory:

```bash
ls
```

Output:

```text
inhere
```


Next, move into the directory:

```bash
cd inhere
```

List the files:

```bash
ls
```

Output:

```text
-file00  -file01  -file02  -file03  -file04
-file05  -file06  -file07  -file08  -file09
```

![level450](images/level450.png)


## Step 2: Identify the human-readable file

Instead of opening every file one by one, we can use the `file` command to determine the type of each file.

```bash
find . -exec file {} + | grep text
```

Output:

```text
./-file09: Motorola S-Record; binary data in text format
./-file07: ASCII text
```

![level452](images/level452.png)

### Understanding the command

* `find .` searches the current directory.
* `-exec file {} +` runs the `file` command on every file that `find` discovers.
* `grep text` filters the results to show only files containing the word **text**.

Although two files contain the word **text**, the hint specifically says the password is in the **only human-readable file**.

* `ASCII text` is plain, human-readable text.
* `Motorola S-Record` is a text-based representation of binary data used for programming embedded devices. Although it contains the word *text*, it is **not** intended to be human-readable.

## Step 3: Verify the files

First, I checked `-file09`:

```bash
cat ./-file09
```

The output was unreadable characters, confirming that it was not the correct file.


Finally, I opened the actual human-readable file:

```bash
cat ./-file07
```

This displayed the password for **Bandit Level 5**.

![level453](images/level453.png)

<details>
<summary>Click here to see the password</summary>
6C7h9GD8M6ai5nr7wo1RonrzFjj9yIrG
</detail>

## What I Learned

* The `file` command identifies the type of a file.
* `find` can execute commands on every file in a directory using `-exec`.
* `grep` filters output to display only matching lines.
* Not every file containing the word **text** is actually human-readable.
* Reading the challenge hint carefully helps determine which result is the correct one.
