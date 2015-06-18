# Learn command line

Please follow and complete the free online [Command Line Crash Course
tutorial](http://cli.learncodethehardway.org/book/). This is a great,
quick tutorial. Each "chapter" focuses on a command. Type the commands
you see in the _Do This_ section, and read the _You Learned This_
section. Move on to the next chapter. You should be able to go through
these in a couple of hours.


---

Make a cheat sheet for yourself: a list of commands and what they do, focused on things that are new, interesting, or otherwise worth remembering.

hostname - my computer's network name
pwd - print working directory
cd - change directory
ls - list directory
mkdir - make directory
rmdir - remove directory
pushd - push directory
popd - pop directory
cp - copy a file or directory
mv - move a file or directory
less - page through a file
cat - print the whole file
xargs - execute arguments
find - find files
grep - find things inside files
man - read a manual page
apropos - find what man page is appropriate
env - look at your environment
echo - print some arguments
export - export/set a new environment variable
sudo - become super user root which is dangerous
chmod - change permission modifiers
chown - change ownership
exit - exit the shell

---


---

What does `ls` do? What do `ls -a`, `ls -l`, and `ls -lh` do? What combinations of those flags are meaningful?

ls shows you the files in the the current directory
ls -a will list all files including the hidden files
ls -l will list the files along with the file details
ls -lh will list the files with the details and the size in a more familiar format

You can combine the flags in order to help you sort the list in a specific way, ie by size or date modified.
---


---

What does `xargs` do? Give an example of how to use it.

xargs can help you perform a function multiple times by having that function loop over a list.This is helpful so that you can quickly perform actions on a large scale. So lets say we had a bunch of files with data in them that we wanted to concatenate to create one file with all of the data.  xargs can loop over the files quickly and ad them all to one file.  

---
