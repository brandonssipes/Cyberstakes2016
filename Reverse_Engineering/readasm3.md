If you don't know how to read assembly then these problems are always a chanllenge so if you know nothing then go back and read 
up on assembly and x86. They give <a href="http://codearcana.com/posts/2013/05/21/a-brief-introduction-to-x86-calling-conventions.html">this</a> 
as a source of reference to x86.  Once you understand that this question should become do able.


>If the esp register has the value 0xbfffee20 at the beginning of this sequence of instructions, what is esp's value after these instructions are executed? Assume that we are using standard 32-bit x86 linux calling conventions.
```
8049860: add $0x74, %esp
8049863: pop %ebx
8049864: pop %esi
8049865: pop %ebp
8049866: ret
```
Answer in decimal

Open up in windows your calculator and change the view to programmer.  Change the setting to Hex and do the math.
We learned by google and probably that document that was link that pop adds 4 to esp and ret adds 2.
So bfffee20 + 74 + 4 + 4 + 4 + 2 = BFFFEEA2.  
It wants that in decimal so change the setting to decimal and it automatically converts it.  Our answer is: 3221221026


