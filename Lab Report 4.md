# Lab Report 4
## Part 1

In `DocSearchServer.java`, we changed the name of the `start` parameter of `getFiles`, and all of its uses, to be instead called `base`.

This was done in exactly 25 steps.

While in vim, first type `/start<Enter>` (7 keys) and you will get something like this below.

![Image](Lab Report 4 Screenshots/startEnter.png)

What is happening here is a search for the word `start`, since that is the word we are trying to replace. This is basically similar to using `Ctrl + F`. When typing `/start<Enter>`, the cursor will jump to the first letter of the first instance of `start`.

Then, type the letters `cgn` (3 keys) and you will get this below.

![Image](Lab Report 4 Screenshots/cgn.png)

We know `gn` selects (highlights) the next match of `start` everytime we use it. It's `start` since that is what we searched for earlier using `/start`. Then, append `gn` to `c` creating `cgn`. `c` deletes the highlighted portion of what we highlight and enters insert mode. This is why the command `cgn` here will delete `start` and enter insert mode.

Now, type `base<Esc>` (5 keys) and see the output below.

![Image](Lab Report 4 Screenshots/baeesc.png)

Since `cgn` put us into insert mode, we type base, since we want to replace `start` with the word `base`. Pressing `<Esc>` will escape us out of insert mode and back to visual mode.

Then, we are going to press `n.` 3 times. (6 keys). 

The first `n.` takes you here:

![Image](Lab Report 4 Screenshots/n1.png)

The second `n.` takes you here:

![Image](Lab Report 4 Screenshots/n1.png)

The third `n.` takes you here:

![Image](Lab Report 4 Screenshots/n1.png)

I didn't tell you to do a 4th one but if you accidentally did or if you're confused on your own when you are done finding and replacing, if you do `n.` again, you get an an error telling you there is nothing left to find and replace.

![Image](Lab Report 4 Screenshots/nerror.png)

What `n.` does each time in these screenshots is simple. `n` is simply go to the next time `start` exists in the file. If it doesn't exist, you get an error like you see on the 4th image of trying it. Appending the `.` repeats the last edit we did, which was doing the command `cgn`, typing `base` and then exiting insert mode. `.` performs all 3 of those actions in one and has now essentially created a find and replace method.

Next type `:wq<Enter>` (4 keys) and you will get the output below.

![Image](Lab Report 4 Screenshots/wqenter.png)

When you type `:wq`, it will show at the bottom left of the terminal where we have previously seen where insert mode, `n.`, `cgn`, and other commands show up. Hitting `<Enter>` will execute this command. `:wq` is a mix of 2 commands where `w` saves the file and `q` quits. Doing this command together, `:wq` will save the file and exit out of vim.

The total keys pressed was: 24.

## Part 2
