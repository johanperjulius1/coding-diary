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

#### Katas solved:
0