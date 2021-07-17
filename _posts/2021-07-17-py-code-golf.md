---
layout: post
---

Code golf is attempting to write code in the least amount of characters. Following are Python code golf tips I collected from around the internet.

```python
#Type Casting
t=range(5);print([*t],{*t},(*T,))
```
```python
#Conditionals
return(b,a)[a<b]
```
```python
#Lambda recursion
f=lambda x:1if x==0else x*f(x-1);f(50)
```
```python
#Nested loops
for k in range(m*n):do_stuff(k/n,k%n)
  #instead of
for i in range(m):
 for j in range(n):  do_stuff(i,j)
```
```python
#List of chars out of a string
s=['a','b','c','d','e']
s=list('abcde')
*s,='abcde'
```
```python
#Increment-Decrement
For integer n, you can write
n+1 as -~n
n-1 as ~-n
```
```python
#Range
for i in[1]*8:foo(i)
```
```python
#Alphabets
map(chr,range(65,91))
```
```python
#Switch
exec{1:"runThisCode()",2:"runThisOtherCode()",3:"runThisOtherOtherCode()"}[a]
{1:runThisCode,2:runThisOtherCode,3:runThisOtherOtherCode}[a]()
exec{1:"runThisCode()"}.get(a,"defaultCode()")
```
```python
#Ceil and Floor
n//1      #floor
-(-n//1)  #ceil
```
```python
#Append
A+=B, #same as A.append(B)  
```
```python
#Multiple imports
o,s,j = map(_import_,['os','sys','json'])
```
```python
#Nested exec
print(eval("f("*k+'1'+")"*k)) #same as f(f(f(f(f(1))))) 
```
```python
#Modular inverse
pow(38, -1, 97) #23
```
```python
#Conditionals
>>> pow(38, -1, 97)
if all(map(isdigit,[a,b,c])) #if isdigit(a) and isdigit(b) and isdigit(c)  #any for or
```
```python
#List assignments
l.insert(x,y) # before
l[x:x]=y,     # after

l.reverse()   # before
l[::-1]=l     # after

l.append(x)   # before
l[L:]=x,      # after (where L is any integer >= len(l))

l[:]=x        # set the contents of l to the contents of x
```
```python
#Swap
a,b=b,a
```
```python
#Sin and Cosine
p=1j**(d/90.)
s=p.real
c=p.imag
```
```python
#List Twin-Primes
p=lambda n: 1 if ([i for i in range(1,n) if n%i==0]==[1]) else 0
[print(i,i+2) for i in range(1,3001) if(p(i)and p(i+2))][0]
```
```python
#Factorial
f=lambda x:0**x or x*f(x-1);f(10)
```
```python
#Say you want to output P if x>0, N if x<0, and Z if x==0.
"ZPN"[cmp(x,0)] #Obsolete
```
```python
#Even or Odd
~n&1 #1 if even
```
```python
#Primality Check
n=int(input());print([i for i in range(1,n) if n%i==0]==[1])
```
```python
#Filter
print(list(filter(lambda a : a>10,[1,2,4,5,66,8,9,5,8,88])))
```
```python
#Fibonacci
def _(a,b):print(a);a,b=b,a+b;_(a,b)
_(1,1)
```
```python
#List Eevee-lutions
s=input()
a=dict(W='Vapor',E='Jolt',F='Flar',P='Esp',D='Umbr',G='Leaf',I='Glac',f='Sylv');print(a[s[0]]+'eon') 
a='wVapor eJolt fFlar pEsp dUmbr gLeaf iGlac FSylv';s;[print(i[1:]+'eon')for i in a.split()if s[0]==i[0]][0]
```
```python
#Number comparison
p=print;s=lambda a: p(2)if a<0else p(3);s(12)
a=int(input());b=(3,2)[a<0];p(b)
p((2<3)*2-1) #-1:false
```
```python
#128 B hex digest generator
f=lambda m:''.join(str(hash(i)%10000010) for i in m);print(hex(int(f(f(input()))))[2:34])
```
```python
#Fizzbuzz
for i in range(n):print((i%3<1)*"Fizz"+(i%5<1)*"Buzz" or i)
```
