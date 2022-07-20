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


