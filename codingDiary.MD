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