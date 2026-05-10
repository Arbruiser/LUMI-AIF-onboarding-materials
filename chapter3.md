---
layout: default
title: "Chapter 3: The Command Line – Your Primary Tool"
nav_order: 3
---

# Chapter 3: The Command Line – Your Primary Tool

In the previous chapter, you successfully logged in to LUMI. If you were successful, you can see LUMI's login wolf, a login "Did you know?" fact, and your command line prompt that looks similar to this: 

```bash
<username>@uan01:~>       
```

#### Welcome to the Shell.

This is the "Command Line Interface" (CLI). It might feel like you've traveled back in time to the 1980s, but in the world of Supercomputing and AI, this is the most modern and powerful way to work.


Read the first 4 chapters of the [Linux Command Line guide](https://ubuntu.com/tutorials/command-line-for-beginners#1-overview). 
If you are more of an auditory learner or if this guide simply wasn't enogh for you, please watch this [video guide](https://www.youtube.com/watch?v=16d2lHc0Pe8).

# Practice
The best way to learn after having studied some theory is to **practice**. Let's apply some things you've learned in the guides in our Command Line terminal on LUMI. You can watch and repeat after this video (???) or follow these step-by-step instructions:

1. When you log into LUMI using `ssh` as we did in Chapter 2, you end up in your user's $HOME directory (this is the current 'working directory'). Check it by running:

```bash
pwd
```

The output should be `/users/username`. This is "where you are" now. 

2. Create a new directory and name it 'first_dir':

```bash
mkdir first_dir
```

If it was successful, there is no output. Check the result by **l**i**s**ting all the files and directories in the current working directory:

```bash
ls
```

You should see your new directory there. 

3. Change your working directory to (or "step into") the new directory: 
```bash
cd first_dir
```

4. While in the new directory, create a new text file using `nano`, a very simple text editor: 

```bash
nano first_file.txt
```

Copy paste something into it (if pressing **ctrl+V** doesn't work, try **ctrl+shift+V**). Save the file by pressing **ctrl+S**. Exit by pressing **ctrl+X**. To help you remember the key combinations, "S" in this case stands for "Save", and "X" stands for "e**X**it". 

{: .note }
> **Note:** The command `nano <filename>` is used to open an existing file or create a new file with that name if it doesn't exist. 

5. Look at the file - `less first_file.txt`. To stop viewing the file, press **ctrl+Z**. 

{: .note }
> **Tip:** Instead of typing the whole name of an existing file (such as in step 5), you can type the first few characters of its name and press Tab. If there are multiple files that start with the same few characters, press Tab twice to see available options. 

6. Next we will upload an image from your machine (PC/laptop) to LUMI. For now, we will do it through the "simpler" web interface:
> a. Open [www.lumi.csc.fi](www.lumi.csc.fi) in your browser (don't close your terminal!), log in and go to `Home directory`. This is your `$HOME` user directory where we were working in the previous steps. There you should see our `first_dir` with `first_file.txt` in it.
> b. Click "Upload" and upload your image to your `$HOME` directory. 

{: .note }
> **Tip:** Another, more 'professional' way of uploading files is to use `scp` command as [described here](https://docs.lumi-supercomputer.eu/firststeps/movingdata/).

7. Open your terminal. Go back to the "parent directory" of the current working directory: 

```bash
cd ..
```

Now, when you're in your `$HOME` directory you should see the file that you uploaded there (Hint: use `ls` to check that it's there).

8. Let's **m**o**v**e our uploaded picture to our new directory. Substitute `<your_image.png>` with the actual name of the image and run:

```bash
mv <your_image.png> first_dir
```

Change your working directory to `first_dir` and list the files in it. Hint: look at steps 2 and 3.

9. Rename the new image to `renamed_image.png`. Make sure to keep the same file extension -`.png`, `.jpeg` or any other that your image has. To rename the image, you use the same `mv` command as it's basically moving the file under a new name to a new (or the same) location:

```bash
mv <your_image.XXX> renamed_image.XXX
```

10. Great job! Now you can disconnect from LUMI by pressing **ctrl+D**. If it outputs `There are stopped jobs.`, press **ctrl+D** once again. The command prompt has changed to `your_username_on_your_computer @ the_name_of_your_computer`, which means that you're back to **your machine** in the terminal. 