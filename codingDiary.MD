## This is my coding diary:

### 2020-23-11
Working on ruby udemy course:

The project is the area code dictionary.

#### Learnings:
- Using a loop to run an entire program
- Again, remember to add a break if to any loop

#### Questions:
- How can I use this piece of code with symbols instead?

dial_book = {
"Orebro" => "702",
"Stockholm" => "100",
"Gothenburg" => "200",
"Malmo" => "300",
"Uppsala" => "400",
"Vasteras" => "500",
"Linkoping" => "600",  }

#### Look-up:

----------------------------------------------------

### 2020-24-11

#### Learnings:

#### Questions:

#### Look-up:

#### Katas solved: Regex validate PIN code
https://www.codewars.com/kata/55f8a9c06c018a0d6e000132/

- Best Practice:
def validate_pin(pin)
  pin.match? /\A\d{4}(\d{2})?\z/
end

or:

def validate_pin(pin)
  (pin.length == 4 || pin.length == 6) && pin.count("0-9") == pin.length
end

- My solution:

def validate_pin(pin)
  if check_string(pin) == true && (pin.length === 4 || pin.length === 6)
    return true
  else
    return false
  end
end

def check_string(pin)
  if pin.scan(/\D/).empty?
    return true
  else
    return false
  end
end

Learning:

Action point: Need to learn regex.

##### Find Maximum and Minimum Values of a List

def min(list)
  list.min
end

def max(list)
  list.max
end

Learning: Passing and using arguments in a function

Action point:

##### Remove first and last character of a string:

- Best Practice:
def remove_char(s)
  s[1...-1]
end

This modifies s by changing the range to start at index 1 instead of 0, and in the end to count from -1 but not include it. An alternative would be

s[1..-2]

- My solution:

def remove_char(s)
 x = s.split("")
   x.shift
   x.pop
   s = x.join
   p s
end

### 2020-27-11
I looked into hashes more

#### Learnings:
myhash.each do end / myhash { |some_key, some_value | puts this}


#### Questions:
1. Måste man alltid ange både key och value?
2. Hur ser kopplingen ut mellan some_key, some_value och det som kommer efter andra | ?
3. Vad heter de olika delarna i each metoden?



#### Look-up:
I want practice ternerays in ruby and in JS

#### Katas solved: 1 - Calculate BMI in ruby

### 2020-28-11
I worked with the console to modify styling in css in our php wordpress sites.

#### Learnings:
myhash.each do end / myhash { |some_key, some_value | puts this}


#### Questions:

#### Look-up:
I want to practice ternary operators in ruby and in JS

#### Katas solved:


### 2020-12-01
Remade area code / dial book challenge.
#### Learnings:
I remade the dial book with symbols instead of strings. Didn't work in the final stage though.

#### Questions:

#### Look-up:

#### Katas solved: 1 - Beginner Series #4 Cockroach

---------------------------------------------------
### 2020-12-02
Starting with a Kata in ruby. Then moving to JS and udemy ninja course.
#### Learnings:
Learning about property vs methods in JS.
.lentgh is a property. .toUpperCase() is a method. Methods ned to end with () to be called.

Learning to call and console string methods in JS.

Learning about operators.

NaN stands for Not a Number

Jag kallar på element i Arrays på samma sätt i javascript som i ruby

ninjas[1] = 'Fabian' This is how I replace a value in an array

.join() slår ihop alla elements i en array till en string.

Loose vs Strict comparison: == vs ===. Med == kan olika typer / classes, t.ex. '25' och 25 vara samma men inte med strict.

#### Questions:

Använder jag .push() eller .push[] för att lägga till ett värde till en Array i ruby?

För push är det () med pop räcker arrayName.pop, men går med () och [] (Det har ingen effekt eftersom vi ändå bara tar bort sista värdet)

Destructive methods = methods som ändrar ursprunglig array

#### Look-up:

#### Katas solved: 1 in ruby - Alternating Cases

### 2020-12-03

#### Learnings:
Control flow: Controlling the flow of our code with conditionals, if statements, loops, ternary operators


for loop in javascript has 4 initial elements;
- Initialisation variable. Can be i = 0; for example.
-Then we have a conditional. Can be for example i < 5;.
- Final expression. Can be i++
- The code block in curly brackets. As long as the condition is true, the code block will run once and then go to the final expression and then start over.


while loops: Don't have all the first three, only the condition. Instead we put the final expression in the code block, as an example i++ in the end.


Do While Loops
Sometimes we want the code block to execute once no matter if the condition is true or not.

Take while and the condition, move it to after the code block instead of before, then add a do to the before of the code block.


Conditional statements - If statements.
We are not using a count element because we only
execute the code block once, if the conditions

#### Questions:

#### Look-up:

#### Katas solved: 1 - Will you make it?

----------------------------------------------------
### 2020-12-04

#### Learnings:
In Ruby, when working with attributes of a class, we want work with instance variables. Börjar med @.

Classes, som default, har en metod som heter

def to_s
end
När jag försöker print out a class, it default to to_s method and prints out what is in it. By default, we don't have anything in there, so for starter we print whatever the method comes up with by default. Det kan jag ändra på genom att definiera to_s till något.

En class, om jag inte använder attr_accessor :xx, :yy, behöver setter och getter method likt dessa.

  <!-- # def first_name=(name)
  #   @first_name = name
  # end

  # def first_name
  #   @first_name
  # end -->

Med attr accessor behövs de dock inte. Jag kan skapa nya instances med Class.new = zzz. Jag använder initialize funktionen i en klass för att ge startvärden

Byter till JS efter lunch
Working with logical operators
#### Questions:

#### Look-up:

#### Katas solved: 1, ruby - Find the middle element
----------------------------------------------------
### 2020-12-05

#### Learnings:

sort_by is a function.
The core of sorting is that to be able to sort, which requires comparing, elements need to be of the same data type. Start by making sure that what you have is of the same data type.

This is for a hash:

arr.keys.map(&:to_s) this converts all keys to strings.

add .sort_by do |str|
  str.length
end

#### Questions:

#### Look-up:

#### Katas solved: 1, ruby - Sort array by string length

def sort_by_length(arr)
arr = arr.sort_by {|x| x.length}
end
or
arr = arr.sort_by(&:length)
or
arr.sort{|x, y| x.length <=> y.length}

----------------------------------------------------
### 2020-12-06

#### Learnings:

no one-function way to sort and integer in ruby. All solutions seems to convert to string then sort then convert back to integer.
One solution did use .digit method though.

#### Questions:

#### Look-up:

#### Katas solved: 1, ruby - Descending Order

----------------------------------------------------
### 2020-12-07

#### Learnings:
JS: Switch statements will execute all code in happy case but also all code for all cases AFTER Happy case. If first is happy, then all of them. If 3rd is happy then 3rd and all after.

if I declare a variable and then change it in and if statement, it is globally (below the if) going to be the new value.
I can't redeclare a variable globally, but inside an if statement for example, I can. let and const only has block-scope. It a variable is not defined in the block, it takes the value that the variable have in the closes block outside. That is with nested blocks. A variable globally can never access a nested (a variable inside a code block.)


In JS, functions fall in the object category.

Calling and invoking a function is the same thing.
Function declaration: giving the function a name and a piece of code that will be executed when invoked.

Function expression: storing a function in a variable (instead of giving it a name when declaring it?). At the end of an expression, after brackets, we shall always have comma, ;. One of the few cases where we will have a comma at the end of a code block. Can then be invoked with variable name followed by parenthesis.

A decleration is when we don't store a function in a variable.

One of the differences between expressions and declaration is hoisting. With declarations, a function is hoisted to the top and can then be used before being declared.

Arrow functions does not work with declarations


#### Questions:

#### Look-up:

#### Katas solved: 1, ruby - Round up to the next multiple of 5


----------------------------------------------------
### 2020-12-08

#### Learnings:

- RUBY
To capitalize each word in a string I convert it to an array and then use an enumerable method like map.
Map returns a new array with modification, each returns the old array unchanged


What is Enumerable?

Enumerable is a collection of iteration methods, a Ruby module, and a big part of what makes Ruby a great programming language.

Enumerable includes helpful methods like:

map
select
inject
Enumerable methods work by giving them a block.

In that block you tell them what you want to do with every element.

- JAVASCRIPT

Varje gång man tar en variabel och sätter lika med något så är det ett expression.
Man kan sätta default values i argument genom att sätta argumentet lika med något. Om man sen inte skickar in rätt antal argument skickas default istället (för
de argument som saknas)

Glöm inte lägga till return när jag definierar en funktion om jag vill att den faktiskt ska returnera något.

Om jag använder en funktion soma argument i en annan funktion så kallas funktion jag för in som argument för en callback function.


#### Questions:

#### Look-up:

#### Katas solved: 1, ruby - Jaden Casing Strings


### 2020-12-12

#### Learnings:


#### Questions:

#### Look-up:

#### Katas solved: 1, ruby - Anagram Detection




























