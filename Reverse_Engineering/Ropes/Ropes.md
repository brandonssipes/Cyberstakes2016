<p>Now we begin to learn the "Ropes" of reverseing.<br>
Program: <a href="https://github.com/zetheroth/Cyberstakes2016/blob/master/Reverse_Engineering/Ropes/ropes">Ropes</a>
<br>
We have already looked at some assembly but now we get to look at and actual executable program.
The first thing you always do for these challenges is run the files command.  That tells you generally what you are working with.
Here it tells us that it is a ELF executable file.
<p>
<br>
This one takes a string in as the input and tells you whether or not it is the flag.
<br>
"But I've never done reverse engineering before, I don't even know where to start with this."
<br>Well the first thing you learn to do is run the strings command. <br>
This is a command that prints out all the printable characters in a file.  This is like the basics of the basics. <br>
We see things that are being called, some of them look like they could be flags. But, if we scroll up. Lo and behold, we see:
```
Usage %s FLAG
get_it?_because_ropes_are_like_strings_43dee7f9
Sorry, that is not the flag
Yes! that is the flag!
```
We know that it is looking for FLAG as input and then it outputs either an error message or a congratz message. In the middle there is the 
flag.


