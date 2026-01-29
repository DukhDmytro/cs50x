Data types
int - for variables to store integer 3 4 5 
integers take up 4 bytes of memory (32 bits). -2^31 to 2^31
unsigned int
unsigned - qualifier, modifies data type. 0 to 2^32. Also there are other qualifires as long short

Char
char data type is used for variables that will store single character
char - 1 byte (8 bit) -127 to 127

Float
float data type is used for variables that will store floating-point numbers aka real numbers
float - 4 bytes (32 bits), so we are limited in how precise we can be.

Double
for real number, they can fit 8 bytes (64 bits)
doubles allow to be specify much more precise real numbers

Void
void a type but not a data type
Used for functions that dont return a value
Parameter list of function can also be void. It mins the function takes no parameters
For now you can think of void as plaseholder for nothing, bur it more complex.

Bool
bool is not built-in in C, but it is in cs50 library
bool can store 2 values true or false

String
string is not built-in in C, but it is in cs50 library
string data type used for variables to store series of characters like word, sentences.

Create a variable
int number;
char letter;
int height, width; - create 2 variables of same data type

int numer; - variable declaration
number = 17; - variable assignment
int number = 17; - variable initialization, declaration and assignment at same time.


Operators
= assignment operator, allows to put a value into variable
Arithmetic operators
+, -, *, /
int x = 2 + 2
x = x * 5
% modulus operator, which gives us the reminder when the number of the left of the operator is dividet by number on the right
int m = 13 % 4
m value is 1
shorthand way to apply arithmetic operator to a single variable
x = x + 5
x += 5
x++
x-- 
incremeting or decrementing by 1
boolean expressions
boolean expressions are used in C for comparing values, evaluate to one of two possible values true or false
in C every nonzero value is equivalent to true, and zero is false

two main types of boolean expressions are logical operators and relation operations
logical AND (&&) is ture if and only if both operands are thrue, otherwivse false
true && true = true
false && true = false
true && false = false
false && false = false

logical OR(||) is true if and only if at list one operand is true, otherwice false
true || true = true
true || false = true
false || true = true
false || false = false

logical NOT (!) - inverts the value of its operand
!true = false
!false = true

relation operators
< less than
<= less than or equeal
>
>=
== equality
!= inequality

conditional statemets, conditional branch
conditional expressions allow program to to make decision and take different fork in the road
if (boolean-expression)
{
    if boolean-expression evaluates to true, all lines of code between the curly braces will execute
    if to false, those lines of code will not ececute
}

if (boolean-expression)
{
if boolean-expression evaluates to true, all lines of code between the curly braces will execute
}
else
{
if boolean-expression evaluates to false, all lines of code between the curly braces will execute
}

if () {}
else if () {}
else if ()
else {}
each branc is mutually excluseve

switch statement is conditional statement that permits enumeration of discrete cases, instead of relying on boolean expressions

int x = get_int();
switch(x)
{
  case 1:
    //do something
    break;
  case 2:
    //do something
    break;
  case 3:
    //do something
    break;
  default:
    //do something
}
it is important to break; between each case, or you will "fall through" each case (unless that is desired behavoir)
switch(3)
{
  case 3:
    printf("3\n");
  case 2:
   printf("2\n");
  case 1:
    printf("1\n");
  default:
    printf("blast off\n");
}

ternary operator
int x = (expr) ? 5 : 6; x will be 5 if true, if false - 6
same as
int x;
if (expr)
{
  x = 5;
}
else 
{
  x = 6;
}

Loops
loops allows to execute lines of code over and over repitedly

while (boolean expression)
{
  the lines of code between {} will execute repeatedly from top to botoom until the boolean experssion evaluates to false
}

while (ture)
{
  infinite loop
  the lines of code between {} will execute repeatedly from top to botoom until and unless we break out of it (with break; statement)
}

do
{
  //code
} while (boolean-expr);

this loop execute all lines of code between {} once, and than, if b evaluetes to true will go back and repeat the process until b evaluates to false. garatie to execute at least 1

for loop used to repeat body of loop specified number of times
for (int i = 0; i < 10; i++)
{
  //body
}
the proces undertaken if a for loop is
the counter variable(s)  is set
the boolean epression is checked
  if it evaluetes to true, execute the body
  if false loop does not execute
the counter bariable is incremented
the boolean expression is checked again
etc.

use cases
while  - you want to repeat a loop an unknown times or not at all
do while - repeat loop an unknown times but at least once
for - repeat a discrete number of times

linux command line
ls - will give you readout of all the files and folders in your current directiry
cd <directory> - change directory, navigate 
. - current folder
.. - parent directory
pwd - present working directory
clear = control+l - clear CLI
~ - home directory
cd - cd to ~
mkdir <directory> - create new subdirectory called <directory> located in current directory
cp <source> <destenation> - copy. create duplicate of the file <source> which will be saved in <destenation>
cp -r <source directory> <dest dir>  -r stands for recursece, and tells cp to dive down into directory and copy everything inside of it (including subrirectories)

rm <file> - remove a file after you cofirm
rm -f <file> - remove without confirmation, use at our own peril, there is no undo
rm -r <directory> - remove directory
rm -rf - to combine -r and -f

sparingly, with caution

mv <source> <destenation> - move. rename a file from source to destenation

directly writing constants into our code is referred as magic numbers, generally try to avoid them.
#define NAME REPLACEMENT - preprocessor directive (also colled macro) for creating symbolic constants/
at the time program is compiled #define goes through code and replaces name with replacement
#include similiar to copy/paste
#define to find/replace
