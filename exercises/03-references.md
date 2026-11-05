# Exercise 3: Reference Drills (S13 homework)

Every snippet below uses the `Pet` class from `src/ObjectLab.java`:

```java
Pet(String name, int age)   // sets both
Pet(String name)            // age starts at 1
getName()   getAge()   birthday()   // birthday() adds 1 to age
```

For snippets 1 to 6: **draw** the variables and objects (a box per object, an arrow per reference variable), then write the output. Do this BEFORE you run anything. Draw on paper and paste a photo link, or sketch it as text in the picture box.

## Snippet 1
```java
Pet a = new Pet("Rex", 3);
Pet b = new Pet("Rex", 3);
a.birthday();
System.out.println(a.getAge() + " " + b.getAge());
```
Picture:

a ----> pet (Name: Rex and age 3);
b ----> pet (Name: Rex and age 3);
object a increases in age by 1
Output:

4 3 

## Snippet 2
```java
Pet a = new Pet("Rex", 3);
Pet b = a;
a.birthday();
System.out.println(b.getAge());
```
Picture:

a ----> pet (Name: Rex and age 3);
b ----> a
object a and b increace by 1, because object b is a refrence variable for a
Output:

a
## Snippet 3
```java
Pet a = new Pet("Mia");
Pet b = new Pet("Zed", 9);
b = a;
b.birthday();
System.out.println(a.getAge() + " " + b.getName());
```
Picture:

a----> pet (Name: mia and age 1);
b----> pet (Name: zed and  age 9);
b----> a (Name: mia age 1);
object b in creaces by 1
Output:
2 mia
## Snippet 4
```java
String s = "Java";
String t = s;
s = s + "!";
System.out.println(s + " " + t);
```
Picture:

s ----> java
t ----> (also java)
s + ! ----> java!
Output:

java! java
## Snippet 5
```java
int x = 5;
int y = x;
y++;
System.out.println(x + " " + y);
```
Picture: 
x ----> 5
y ----> (also 5)
y++ ----> y+1
Output:
5 6
## Snippet 6
```java
Pet a = new Pet("Rex", 3);
Pet b = a;
a = null;
System.out.println(b.getName());
```
Picture:

a ----> pet (rex age 3)
b ----> a (also rex age 3)
a ----> turns to nothing
Output:
Rex
## Snippet 7 (this one crashes)
```java
Pet a = new Pet("Rex", 3);
Pet b = a;
a = null;
b = null;
System.out.println(a.getName());
```
- Exception name: nullpointerecepcion
- Line that crashes: last line
- Which variable is null? both
- Your fix (one line of code): get rid of line 3

## Snippet 8: write your own
Write a snippet where two variables alias one `Pet`, then explain its output in two sentences.

```java
pet a = new pet("James", 8);
pet b = a;
pet c = a;
b.birthday();
System.out.println(a.getName() + " " + b.getName() + " " + c.getName());
System.out.println(a.getAge() + " " + b.getAge() + " " + c.getAge());

```

Explanation:

here we have the original varieble a that 
## Checked my predictions
Which snippets did I get wrong, and what was I assuming?
