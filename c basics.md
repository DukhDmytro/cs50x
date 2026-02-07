Data types
why does C cares about data types?
all information in computers stored in bites, 01000001 - can be 'A' or 65. tell the computer it is letter or int
int (data type) balance (variable name) = (assignment operator) 20 (value to assign);
create int named balance that gets value 20. - statement
convey

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
use 1 byte. Достатьно і 1 біт, але виявляється що 1 байт зручніше викорисотвувати, навіть якщо 7 біт не використовуються.

String
string is not built-in in C, but it is in cs50 library
string data type used for variables to store series of characters like word, sentences.

format codes
%i - int
%f - float %.9f - 9 float digits
%c - char
%s - string 


Create a variable
int number;
char letter;
int height, width; - create 2 variables of same data type

int numer; - variable declaration
number = 17; - variable assignment
int number = 17; - variable initialization, declaration and assignment at same time.

int n = 1; create a variable called n that stores value 1

Operators
= assignment operator, allows to put a value into variable
Arithmetic operators
+, -, *, /
/ - flor division. round down, even if result is closer to up
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

int i = 0 - initialization
i < 10 - boolean expression
i++ - incrementation

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


first things first
out of sight out of mind
take for granted
intercept
commonplace
crunching
circutry
deliberatly
reminicent

int h;
h - garbage value, якесь випадкове значення яке було запичане в пам'яті раніше, і цю пам'ять виділили під змінну, але не присвоїли їй значення.

source code -> compiler -> machine code
make - program
clang - compiler
clang <source code.c> -> output will be a.out (asembler output)
clang <source code.c> -lcs50 - compile code and link cs50 library -l - command line arugemnt <name.c> command line argument
cland -o <name> <source code.c> -lcs50; -o - output name; same as make

compiling consists of 4 separete processes:
preprocessing
    process #, if you use printf(), finds stdio.h and include printf code to your code
compiling
    convert preprocessed code and convert it to assembler code wich computer processor understand
assembling
    convert asembler code to machine code
linking
    combine machine code from libraries with macine code from source code

type casting
(float) 3 - make float 3.0 from 3
1 float value in calculation of int cast result to int

array is chunk of contiguous memory
int scores[3]; - create array of 3 integer - chunk of memory to store 3 ints - 12 bytes of coniguous memory (4 bytes for each int)
indexing 
scores[0] = 72;
scores[1] = 73;
scores[2] = 33;
values of array are contiguous 
const int N = 3; - constant variable. convention to capitalize constant names
float avg(int numbers[]) - pass array to function
string - array of charecters
\0 - 00000000 - 8 zero bits. \0 - NUL - end of the string

string.h - library for strings. strlen function - get length of the string 
cytype - provides many functions for classifying and modifying characters.
math - many functions that allow you to perform mathematical tasks on numbers


functions
aka methods procedures subroutines
частина програми, яка реалізує певний алгоритм і дозволяє звернення до неї з різних частин загальної (головної) програми
функція може приймати декілька аргументів або жодного, та повертати якийсь результат
не обов'язково знати як реалізоівана логіка у функції, достатьо знати які аргументи функція приймає і який результат повертає
для чого використовують функції?
1. організація: за допомогою функцій можна розділити складну задачу на декілька простіших задач, коли певна функція виконує певну частину більшої задачі
2. спрощення: менші компоненти зручніше писати, дебагати. Наприклад є функція яка запитує вхідні данні у користувача, є функція яка їх оборбляє, є функція яка представляє результат, тому якщо буде якась проблема то не потібно дивитись і дебагати весь код, а певну його частину.
3. повторне використання: код у функції потрібно написати 1 раз, а використовувати за потреби скільки завгодно раз. printf у с написана 1 раз, але використовується вже 40 років

функція повинна мати зрозуміле і очевидне ім'я, щоб можна було зрозуміти поведінку функції з її ім'я

function declaration
<return type> <function name> (arguments)
тип данних які повертає функція, її ім'я, набір агрументів які передаються до функції (потрібно зазначати їх тип данних і ім'я)
int add_two_ints(int a, int b);
для того щоб використовувати функцію в main потрібно її оголосити перед main, але це погана практика, бо ми хочемо відразу бачити що робить програма, а не допоміжні функції. Тому перед main вказуються прототипи функцій, які будуть оголошені піся main. Як обіцянка компілятору що ось буде така функція, ти її побачиш пізніше в коді

function definition
int add_two_ints(int a, int b)
{
    // realization of predictable behavoir
    return a + b;
}

function call
int sum = add_two_ints(5, 6); для того щоб виклакати функцію необхідно передати їй підходящі аргументи і присвоїти результат який вона повертає підходящому типу данних.
miscellany
іноді функції можуть не приймати аргументів і нічого не повертати
void foo(void); - функція яка нічого не повертає і не приймає аргументів

scope
scope is caracteristic of varialbe that defines from wich function variable can be accessed
local variables can be accessed within function in which it is created
gloabal variable from any function in program

float x = 0.5;

int main(void)
{
// x is accesseble here and its value can be changed in main
}
int foo(void)
{
// x is accesseble here and its value can be changed in foo
}
local variables in c are **passed by value**
when a variable are passed by value, the **callee (function that is receiving value)** resives the copy of the passed variable and not variable itself
the variable in **caller** is unchanged unless overwritten


**array**
array is data structure used to hold value of same type contiguous in memory
array - block of cotniguous memory partitioned into same size blocks of memory called elements, each of elements can store sertein amount of data (all elements same data type int char ...). Each element can be accessed by index. Indexes start from a zero, last element of array size N has N-1 index. C will not prevent you to access index out of array, code will compile but you get unexpected behavoir or segmentation fault becouse access to memory out of array.

array declaration 
data type name[size];
int numbers[5] - array of 5 integers, indexes 0 1 2  3 4
int numbers[3] = { 1, 2, 3 } or numbers[0] = 1; numbers [1] = 2; numbers[2] = 3; or int numbers[] = { 1, 2, 3 }
int grid[10][10]; - two dimencinal array
each element of array can be treated as variable, but whole array can not be treated as variable
for example you can not assign one array to other to copy array, you need to loop through aray to copy it
in c arrays are passed by reference. Calle gets array itself but not the copy of array

command-line arguments
it is way to pass data to your porgram at running the program
int main(int argc, string argv[]) - collect data from user - argc (argument count) and argv (argrument vector) - what and how much data user provided during running the program
names of argument are conventional names, you can call it whatever you want but this is convention
./greedy 1024 cs50 - argc will be 3, 0 is always program name 1 - 1024, 2 0 cs50. program name counts itself as command-line argument. arguments divided by space
argv - array of strings, each element per string. first elemen index is 0, last argc - 1


design
avoid redundand operations and repetitions of code, use functions to abstract and avoid
code easy to read easy to maintain
avoid magic numbers - use constatns
