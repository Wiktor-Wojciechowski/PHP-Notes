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
