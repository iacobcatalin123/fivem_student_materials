## Operators and Expressions
> In Lua, operators are used to perform arithmetic, comparison, and logical operations on values. Here is an overview of the different types of operators in Lua:

1. ### Arithmetic

`+` : addition

`-` : subtraction

`*` : multiplication

`/` : division

`%` : modulo (remainder)

```lua
a = 10
b = 5
c = a + b -- 15
d = a * b -- 50
e = a / b -- 2
f = a % b -- 0 (because 10 is evenly divisible by 5)
```

2. ### Comparison
These operators are used to compare two values and return a boolean result. The following comparison operators are available in Lua:

`==` : equal to

`~=` : not equal to

`<` : less than

`>` : greater than

`<=` : less than or equal to

`>=` : greater than or equal to

```lua
a = 10
b = 5
c = 10
d = a == b -- false
e = a ~= b -- true
f = a > b -- true
g = b >= c -- false
h = a < b -- false
i = a <= c -- true
```

3. ### Logical
These operators are used to perform logical operations on boolean values. The following logical operators are available in Lua:

`and` : logical and

`or` : logical or

`not` : logical not

```lua
a = true
b = false
c = true
d = a and b -- false
e = a or b -- true
f = not a -- false
g = not b -- true
h = a and c -- true
```
4. ### Others

The concatenation operator (`..`) is used to concatenate two strings.
The length operator (`#`) is used to get the length of a string or table.
Lua also provides some other operators, such as the assignment operator (`=`), the table index operator (`[]`), and the function call operator (`()`).

```lua
a = "hello"
b = "world"
c = a .. " " .. b -- "hello world"


a = "hello"
b = {1, 2, 3, 4, 5}
c = #a -- 5
d = #b -- 5

a = 10
b = {1, 2, 3, 4, 5}
b[3] = a -- assigning the value of 'a' to the 3rd index of the 'b' table
c = b[3] -- 10 (getting the value of the 3rd index of the 'b' table)
d = math.sin(a) -- calling the 'sin' function from the 'math' library with the value of 'a'
```
> In Lua, operators have precedence and associativity rules that determine the order in which they are evaluated. It's important to understand these rules to write correct and efficient Lua code.


## Control structures (if/else, while, for)
> In Lua, control structures are used to change the order in which statements are executed based on certain conditions. Here are the different types of control structures in Lua:

1. ### Conditional
> The if statement is used to execute a block of code if a certain condition is true.

> The if-else statement is used to execute one block of code if a condition is true and another block of code if it's false.

> The if-elseif-else statement is used to execute different blocks of code based on multiple conditions.

```lua
if x > 0 then
  print("x is positive")
elseif x < 0 then
  print("x is negative")
else
  print("x is zero")
end
```

2. ### Loops
> The while loop is used to execute a block of code as long as a certain condition is true.
> The repeat-until loop is used to execute a block of code until a certain condition is true.
> The for loop is used to iterate over a range of values or over the elements of a table.

```lua
for i = 1, 10 do
  print(i)
end

while true do
    print("hello")
end
```

3. ### Flow Control

> The break statement is used to exit a loop.
> The goto statement is used to jump to a specific label in the code.
> The return statement is used to exit a function and return a value.
```lua
while true do
  x = "stop"
  if x == "stop" then
    break
  end
end
```

> In Lua, control structures are often combined to create complex programs that can handle different situations and respond to user input.


## Scope

Lua has two types of scope: global and local.

1. ### Global Scope
> A variable or function defined in the global scope can be accessed from anywhere in the program.
> Global variables and functions are defined outside of any function or block.

```lua
x = 10 -- global variable

function add(a, b)
  return a + b
end -- global function
```

2. ### Local Scope
> A variable or function defined in a local scope can only be accessed within the block or function where it was defined.
> Local variables and functions are defined inside a function or block using the local keyword.

```lua
function multiply(a, b)
  local result = a * b -- local variable
  return result
end -- local function

-- This will result in an error because `result` is not defined in the global scope.
print(result)
```

> It's generally recommended to use local scope whenever possible to avoid naming conflicts and improve performance. Global variables should only be used when necessary and with caution.


## Homework FiveM Resource