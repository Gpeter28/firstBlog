---
layout: post
title: Shenzhen I/O
---

# New #
开了新坑，挺好玩的汇编


## Instruction Operands ##
R Register
I Integer(-999 to 999)
R/I   Register or Integer
P     Pin register(p0, p1, x0 etc)
L     Label


## Basic Instructions ##
nop   no effect
mov R/I R   cp first value to second
jmp L      jump to :L
slp R/I   sleep
slx P    sleep until data is available


## Arithmetic Instructions ##
**If the value out of range(-999 to 999) it will be store in the closest num;**


add R/I add the value to the acc register and store in it
sub
mul

not     if value in acc is 0, store 100 in acc.Otherwise store 0

dgt R/I  isolate the specified digit or the value in acc and store in acc.
for example  `acc:596 dgt 0   acc':6` `dgt 1 acc': 9` `dgt 2 acc':5` 

dst R/I R/I set the digit of acc specified by the first operand to the value of the second operand 
example:    `acc:596`    `dst 0 7 acc':597`  `dst 1 7 acc':576`

## Test Instructions ##
teq R/I R/I (test equal)
if( A == B)
do +
else -

tgt R/I R/I  (test greater)
if(A > B)
do + else do 

tlt R/I R/I  (test little?)
if(A < B)
do + else do -

tcp R/I R/I

if(A > B) do +
if(A == B)  nothing happen
if(A < B) do - 





# MC4000 #
