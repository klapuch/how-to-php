# How to php

## Variables
```php
$wrong_variable = "Dont't name variables like that. It is called snake cases and in PHP it is not recommended to use";
$firstname = 'Dominik';
$lastname = 'Klapuch';
$programmingLanguage = 'php'; // Notice the camelCase naming
$php = 'PHP language'; // Notice that name of the variable is same as the value above
$fullname = $firstname . ' ' . $lastname; // Strings are merged by dot (.) char
echo $fullname; // Will output: Dominik Klapuch
echo "$firstname $lastname"; // The same output as above
echo "{$firstname} {$lastname}"; // More readable approach with the same output as above
echo '$firstname $lastname'; // Notice the single quotes. Will output: $firstname $lastname
echo $$programmingLanguage; // Notice the double dollar sign ($). Will output: PHP language
```

### Assigning
```php
$a = $b = $c = 2; // This is the same as: $a = 2; $b = 2; $c = 2;
$name = 'Dominik';
$name .= ' Klapuch'; // $name is now Dominik Klapuch
$name = $name . ' Klapuch'; // The line above is same as the current one
$a = 10;
$a += 5; // The shortcut may be applied for all operators (+=, -=, *=, .=, ...)
$a = 1;
$a += 1; // I want to increment value by one
++$a; // The line above is same as the current one
--$a; // Decrement, same as $a -= 1; 
```

### Types
In php we have several data types, which are built in the language. The types are: boolean (true or false), integer (numbers like -1, 0, 5), float (numbers like 0.5), string (all texts closed in quotes (' or ")), array (bunch of values)

```php
$integer = 10;
$string = 'string';
$string = "string"; // Same as the line above. Use ' instead of "
$float = 0.5;
$boolean = true;
$boolean = false;
$array = [10, 20, 30];
$array = array(10, 20, 30); // Same as the line above. Use [] instead of array
```
#### Array
```php
$books = ['House of leaves', 'The Shining', 'It']; // Variable called $books has all the books
$books = [0 => 'House of leaves', 1 => 'The Shining', 2 => 'It']; // Same as the line above. Array is indexed by 0
echo $books[0]; // Will output: House of leaves
echo $books[1]; // Will output: The Shining
echo $books[2]; // Will output: It
echo $books[3]; // Error. On index 3 there is no value
/**
* But we don't want to access the books through indexes. I would like to access each book by ISBN
* By the way, this is called multiline comment and it is more readable than single line comment (//)
*/
// ISBNs are simplified
$books = ['12-23' => 'House of leaves', '23-44' => 'The Shining', '22-99' => 'It'];
echo $books['12-23']; // Will output: House of leaves
// Indexes must be unique, that's the reason why the array is indexed by ISBNs.
// What if there would be same indexes? Let's see.
$books = ['12-23' => 'House of leaves', '12-23' => 'The Shining', '22-99' => 'It'];
// In fact, the array of books has now only two items. First book House of leaves has been overwritten by The Shining
echo $books['12-23']; // Will output: The Shining
```

### Comparing
```php
var_dump(true == 1); // Same. Will output: true
var_dump(true === 1); // Not same. Will output: false
var_dump(true == 2); // Not same. Will output: false
var_dump(0 == false); // Same. Will output: true
var_dump(0 === false); // Not same. Will output: false
var_dump(0e12345 == 0); // Same. Will output: true
var_dump(0e12345 === 0); // Not same. Will output: false
var_dump(true == 1 && false == 0); // Will output: true becase both condition are true
var_dump(true == 1 || false === 0); // Will output: true, because true == 1 is true
```