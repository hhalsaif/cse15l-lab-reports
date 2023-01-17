## Lab Report
There are many steps included to be able to long into your course-specific account on ieng6. This course requires a couple of tools to be able to do all the required work. These tools include bash, git and VScode.

### VScode 
Lets start with trying to setup VScode.
1. Check if VScode is installed already! 
2. If not you can head to this [link](code.visualstudio.com)
3. Click on the big blue button that says "Download for (OS)"
4. Go through the installation process
5. After finally installing VScode you'll get this pop up and you're done!
![](https://lh6.googleusercontent.com/tylpXh1eORF_hviiMni4PNDD5UqE4m709pNwRVwmydX2N0fecbeP6oDdO7Andz-4Y-bOHcaT-k3ZIuCpV_vTRnUaF7d4T0PUtH-t-eAild4yy3UuRTwnfV-CBLToOfZKm_lzYfLj3lIMTB6Td3u4aqU-JECG3nqetkaXl8V8LSxkCh305N90MZHA9OlHXA)
### Getting Bash and Git

Since we have already installed VScode installed we can use that to check if we have bash and Git setup.

- Open VScode
- Open a new terminal window using ``` Ctrl + Shift + ` ```
- A new window will pop up! 
- From the list of buttons you will see available on the right side of the window you can choose between
	- Close Panel 
	- Maximize Panel Size
	- Kill Terminal
	- Split Terminal 
	- Launch Profile
- Click on launch profile and choose Bash if available
- Maximize Panel!

**If you can't find Git Bash then open this [link](git-scm.com/downloads)**. Click on your operating system of choice and install git bash. After you are done with this process Do the steps mentioned above.

### SSH and Remotely Connecting

SSH can help us with remotely connecting to our machines!
In this case you will be typing out this command: ssh username@ieng6.ucsd.edu substituting username with your class username, but wait I don't know that yet. 

You can head to this [link](sdacs.ucsd.edu/~icc/index.php) and you willl find something that says **Account Lookup** insert your username which is the first part of your email: username@ucsd.edu alongside your Student ID which start with the letter A and a number sequence. Click on submit and you are in! Inside you will find a heading with the name **Additional accounts** under it you can find you class student ID! However, we still have to do one more thing, assigning a password!

Try opening this [link](https://sdacs.ucsd.edu/~icc/password.php) entering your CS15L username this time and student ID. Entering your previous password, this will be your UCSD account password if you have not initialized a password yet and typing a new password. That's it you're all set now! Go ahead and open VSCode and try to ssh using the aforementioned steps.

![](https://lh4.googleusercontent.com/WL67LlpIdCIwll8bySrI2s2A2_UF_4wAH5HlxYTPLLtMmGLDoBl-v39fFn1jES4vhNYE3SWBrDzs_3Xv4ezUOHL6BuCiFLhkmnhZ0Mxw0gAm0bejedl4Imilo-0jTejspEZObUwzM34J-mXEpQP4IBvzAJK-25bhNju7YOPU-d0luTRkX3n9fsnTi6U0HQ)

### Trying out some commands!
> ls - This list all files in current directory
> ls - You can see that you have a new directory called Lab now!
> mkdir Lab - This creates a new directory with the name Lab
> cd Lab - Change Directory to Lab
> touch Hello.java - Touch creates a new file with the specified name (Hello.java)
> cat Hello.java - Cat prints out the constant of a file its empty right now.
> pwd - Prints the current working directory!

![](https://lh6.googleusercontent.com/6H8l_6ru4qoOkUbOn_jbcdTRB5W8tqySAsEgdDwABiE8174LdU85MExyBSqhP-MXU4X_V4lMRUHNSO6BZ4yJg3eNFAmrlEQff8ewa4UIeK0sAFcjpib5zyzltn1Se2guRVLVq4nLswnNlMB4UDjaCC_xBig9H9P3luNna7Y8iBP9Hk3qCwSuZhAU5lTEWw)
