# PHP-Notes

 <?php
$txt = "W3Schools.com";
echo "I love $txt!";
echo "I love " . $txt . "!"; //the output is the same
?> 
 <?php
$x = 5;
$y = 10;

function myTest() {
  global $x, $y;
  $y = $x + $y;
}

myTest();
echo $y; // outputs 15
?> 
PHP also stores all global variables in an array called $GLOBALS[index]. The index holds the name of the variable. This array is also accessible from within functions and can be used to update global variables directly.

The example above can be rewritten like this:
Example
<?php
$x = 5;
$y = 10;

function myTest() {
  $GLOBALS['y'] = $GLOBALS['x'] + $GLOBALS['y'];
}

myTest();
echo $y; // outputs 15
?> 


$txt1 = "hello world"
echo "<h2>" . $txt1 . "</h2>"; // prints out the h2 heading with set text

print similar to echo, differences:
echo is minimally faster, takes multiple arguments and does not return a value
print can take one argument and returns 1

var_dump($x); - returns type and value of variable


$cars = array("Volvo","BMW","Toyota"); 

 <?php
class Car {
  public $color;
  public $model;
  public function __construct($color, $model) {
    $this->color = $color;
    $this->model = $model;
  }
  public function message() {
    return "My car is a " . $this->color . " " . $this->model . "!";
  }
}

$myCar = new Car("black", "Volvo");
echo $myCar -> message();
echo "<br>";
$myCar = new Car("red", "Toyota");
echo $myCar -> message();
?> 

The PHP strlen() function returns the length of a string.
str_word_count()
strrev()
The PHP strpos() function searches for a specific text within a string. If a match is found, the function returns the character position of the first match. If no match is found, it will return FALSE.
echo str_replace("world", "Dolly", "Hello world!"); // outputs Hello Dolly!


is_int()
is_integer() - alias of is_int()
is_long() - alias of is_int()

is_float()
is_double() - alias of is_float()


is_finite()
is_infinite()

is_nan()

/ Check if the variable is numeric   
$x = 5985;
var_dump(is_numeric($x));

echo "<br>";

$x = "5985";
var_dump(is_numeric($x));

echo "<br>";

$x = "59.85" + 100;
var_dump(is_numeric($x));

echo "<br>";

$x = "Hello";
var_dump(is_numeric($x));
